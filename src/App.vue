<template>
  <div id="app">
  	<navbar></navbar>
  	<div class="container">
  		<router-view></router-view>	
  	</div>
  </div>
</template>

<script>
	import Navbar from './components/Navbar.vue'

	export default {
		components: {
			'navbar': Navbar
		}
	}
</script>

<style>

</style>
