<template>
	<v-app>
		<v-main>
			<v-container>
				<v-checkbox v-model="geo" label="geo"></v-checkbox>
				<v-text-field
					label="height"
					v-model="height"
					type="number"
					style="width: 60px"
				></v-text-field>
				<v-color-picker v-model="color"></v-color-picker>

				<LocationPicker
					v-model="location"
					:apiKey="apiKey"
					:geo="geo"
					:height="`${height}px`"
					:color="color"
			/></v-container>
		</v-main>
	</v-app>
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
				geo: false,
				geoOptions: [true, false],
				height: 500,
				color: "#973333ED",
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