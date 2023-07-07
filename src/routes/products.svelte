<script>
	import productos from '../data/products.js';
	import ProductCard from '../components/ProductCard.svelte';
</script>

<div class="product-screen">
	<div class="product-container">
		{#each productos as producto}
			<ProductCard {producto} />
		{/each}
	</div>
</div>

<style>
	.product-screen {
		margin-top: 35px;
		display: flex;
		height: 100vh;
		width: 100vw;
		background-color: beige;
		align-items: top;
		justify-content: center;
		padding-top: 30px;
	}
	.product-container {
		width: 85%;
		height: auto;
		margin-left: auto;
		margin-right: auto;
		background-color: bisque;
		display: grid;
		column-gap: 3px;
	}
</style>
