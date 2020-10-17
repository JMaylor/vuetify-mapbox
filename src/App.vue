<template>
	<div id="app">
		<Form
			:geo="true"
			:initialLocation="[-0.496934, 51.437032]"
			:apiKey="apiKey"
		/>
	</div>
</template>

<script>
	import Form from "./components/Form.vue";

	export default {
		name: "App",
		components: {
			Form,
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