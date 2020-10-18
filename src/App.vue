<template>
	<div id="app">
		<LocationPicker v-model="location" :apiKey="apiKey" />
	</div>
</template>

<script>
	import LocationPicker from "./components/LocationPicker.vue";

	export default {
		name: "App",
		components: {
			LocationPicker,
		},
		data() {
			return {
				location: null,
			};
		},
		computed: {
			apiKey() {
				return process.env.VUE_APP_MAPBOX_KEY;
			},
		},
	};
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>