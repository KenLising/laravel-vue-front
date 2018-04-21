<template>
	<div class="container mb-5">
	    <div class="row justify-content-center">
	        <div class="col-md-8">
	            <div class="card">
	                <div class="card-header">Login</div>

	                <div class="card-body">
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
						
						<button @click="login" class="btn btn-sucess float-right">Login</button>

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
				email: '',
				password: ''
			}
		},
		methods: {
			login () {
				var data = {
					client_id: 2,
					client_secret: 'xvNQ7EXuM0Y1No5Jyk3p8rbwQORgqFYyBxpK4tcl',
					grant_type: 'password',
					username: this.email,
					password: this.password
				}
				this.$http.post("oauth/token", data)
				
				// Old Style function creation
				// .then( function(response) {
				// 	console.log("test")
				// })
				
				// ES 6 JS
				.then(response => {
					// Set Token
					this.$auth.setToken(response.body.access_token, response.body.expires_in + Date.now())

					// Re Route
					this.$router.push("/feed")
				})
			}

		}
	}
</script>

<style>
	
</style>