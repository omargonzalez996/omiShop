<script>
	import Navbar from '../components/Navbar.svelte';
	import Home from './home.svelte';
	import Products from './products.svelte';
	const links = [
		{ url: '#home', text: 'Home' },
		{ url: '#about', text: 'Products' },
		{ url: '#services', text: 'Services' },
		{ url: '#contact', text: 'Contact' }
	];

	let currentPage = '';
</script>

<div class="main-container">
	<Navbar {links} />
	<Products />
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100&display=swap');
	:root {
		font-family: 'Inter', sans-serif;
		background-color: #000814;
		padding: 0px;
		color: white;
		min-width: 600px;
	}
	.main-container {
		position: fixed;
		left: 0;
		display: block;
		top: 45px;
		padding: 0;
	}
</style>
