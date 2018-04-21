<template>
	<div class="container">
	    <div class="row justify-content-center">
	        <div class="col-md-8">
	            <div class="card">
	                <div class="card-header">Register</div>

	                <div class="card-body">
	                	<div class="form-group">
	                		<input
	                			v-model="name"
	                			class="form-control" 
	                			type="text" 
	                			placeholder="Name">
	                	</div>

	                    <div class="form-group">
	                    	<input
	                    		v-model="email"
	                    		class="form-control" 
	                    		type="email" 
	                    		placeholder="Email">
	                    </div>

	                    <div class="form-group">
	                    	<input 
	                    		v-model="password"
	                    		class="form-control"
	                    		type="password"
	                    		placeholder="Password">
	                    </div>
						
						<button class="btn btn-sucess float-right">Register</button>

	                </div>
	            </div>
	        </div>
	    </div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				name: '',
				email: '',
				password: ''
			}
		}
	}
</script>

<style>
	
</style>