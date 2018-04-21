<template>
	<div class="row">
		<product 
			v-for="product in products" 
			:product="product">
				
		</product>	
	</div>
</template>

<script>
	import Product from './Product.vue'

	export default {
		data () {
			return {
				products: []
			}
		},
		components: {
			'product': Product
		},
		created () {
			this.$http.get('api/products')
			.then(response => {
				this.products = response.body
			})
		}
	}
</script>

<style>
	
</style>