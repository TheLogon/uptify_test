<template>
	<div class="home__services">
		<a href="#" class="home__services_item">
			<img src="/images/google-store.svg" alt="" />
			<p class="home__services_name">Google Store</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/gira.svg" alt="" />
			<p class="home__services_name">Gira</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/dropbox.svg" alt="" />
			<p class="home__services_name">Dropbox</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/google-my-business.svg" alt="" />
			<p class="home__services_name">Google My Business</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/automate.svg" alt="" />
			<p class="home__services_name">Automate</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/sales-force.svg" alt="" />
			<p class="home__services_name">Sales Force</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/caltrain.svg" alt="" />
			<p class="home__services_name">Caltrain</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/google-my-business-two.svg" alt="" />
			<p class="home__services_name">Google My Business</p>
		</a>
		<a href="#" class="home__services_item">
			<img src="/images/intelligent-voice.svg" alt="" />
			<p class="home__services_name">Intelligent Voice</p>
		</a>
		<a href="#" v-for="item in info" :key="item.id" class="home__services_item">
			<img :src="item.image" alt="" />
			<p class="home__services_name">{{ item.title }}</p>
		</a>
	</div>
</template>

<script>
	export default {
		name: "services",
		data() {
			return {
				info: null,
			}
		},
		async mounted() {
			this.info = await $fetch("https://fakestoreapi.com/products?limit=3")
		},
	}
</script>

<style></style>
