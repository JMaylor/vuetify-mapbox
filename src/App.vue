<template>
  <v-app>
    <v-main>
      <v-container>
        <v-checkbox v-model="geo" label="geo"></v-checkbox>
        <v-checkbox v-model="searchForm" label="search"></v-checkbox>
        <v-color-picker v-model="color"></v-color-picker>
        <p>{{ location }}</p>
        <LocationPicker
          v-model="location"
          ref="locationPicker"
          :apiKey="apiKey"
          :geo="geo"
          :searchForm="searchForm"
          :color="color"
        />
      </v-container>
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
        location: [],
        geo: true,
        searchForm: true,
        height: 500,
        color: "#FFA500",
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