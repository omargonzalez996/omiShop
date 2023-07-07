<script>
	export let links = [];
	export let logo = '/loguillo.png';
	import Icon from '@iconify/svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		function checkScreenSize() {
			isSmallScreen = window.innerWidth <= 768; // Adjust the breakpoint as needed
		}
	});
</script>

<nav>
	<div class="logo">
		<img src={logo} alt="logo.png" />
	</div>
	<ul>
		{#each links as link}
			<li><a href={link.url}>{link.text}</a></li>
		{/each}
		<div id="my-icon">
			<li>
				<Icon class="carticon" icon="ion:cart-sharp" color="white" width="25" height="25" />
			</li>
		</div>
	</ul>
</nav>

<style>
	nav {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		background-color: black;
		border: none;
		padding: 1px;
		display: flex;
		align-items: center;
		box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px,
			rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px,
			rgba(0, 0, 0, 0.09) 0px -3px 5px;
	}
	.logo {
		height: 50px;
		width: 50px;
		width: 50%;
		display: flex;
		align-items: center;
		justify-content: left;
		padding-left: 10px;
	}
	ul {
		list-style: none;
		display: flex;
		align-items: center;
		justify-content: right;
		height: 46px;
		width: 50%;
	}

	li {
		margin: 0 10px;
	}

	a {
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
		text-decoration: none;
		color: white;
	}
	a:hover {
		color: #0a68ff;
		transition: 0.3s ease-in-out;
	}
</style>
