<script>
    import { onMount } from "svelte";
    export let = producto;

    onMount(()=>{
        console.log(producto);
    })
</script>

<div class="card-container">
	<div class="image">
		<img src={producto.image_url} alt={`${producto.nombre}_image`} />
	</div>
	<div class="title">
		<h2>`${producto.nombre}`</h2>
	</div>
	<div class="description">
		<p>{producto.descripcion}</p>
	</div>
	<div class="details">
		<div class="stock">
			<h2>{producto.cantidad_stock}</h2>
		</div>
		<div class="precio">
			<h2>{producto.precio}</h2>
		</div>
	</div>
</div>
