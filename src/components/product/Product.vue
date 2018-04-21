<template>
	<div class="card col-3 p-2">
	  <img class="card-img-top mt-3" src="http://via.placeholder.com/400x400">
	  <div class="card-body">
	    <h5 class="card-title">{{ product.name }}</h5>
	    <p class="card-text">{{ product.price }}</p>

	    <a href="#" class="btn btn-info">Wish List</a>
	    <a href="#" class="btn btn-success">Buy Now</a>
	  </div>
	</div>
</template>

<script>
	export default {
		props: ['product']
	}
</script>

<style>
	
</style>