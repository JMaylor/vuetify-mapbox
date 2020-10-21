# Vuetify Location Picker

Location Picker for Vuetify JS, using [Mapbox API](https://www.mapbox.com/).

Online Demo

Demo Source Code

## Installation

```
npm install --save vuetify-location-picker mapbox-gl
```

```
import Vue from 'vue'
import LocationPicker from 'vuetify-location-picker'

Vue.use(LocationPicker)
```

## Usage

In your template section:

```
<LocationPicker v-model="location" :apiKey="apiKey" />
```

## Properties

| Name              | Type    | Default Value                         | Description                                                             |
| ----------------- | ------- | ------------------------------------- | ----------------------------------------------------------------------- |
| location (model)  | Array   | []                                    | [longitude, latitude]                                                   |
| apiKey (required) | String  |                                       | [Mapbox API](https://www.mapbox.com/) Key                               |
| geo               | Boolean | true                                  | Whether or not to display button for using browser's geolocation API    |
| height            | String  | '500px'                               | Height of map container.                                                |
| initialLocation   | Array   | [-0.496934, 51.437032]                | Center of map on first load.                                            |
| color             | String  | 'orange'                              | Color of map markers. Can pass any CSS color type                       |
| mapStyle          | string  | 'mapbox://styles/mapbox/outdoors-v11' | [Mapbox style](https://docs.mapbox.com/api/maps/#mapbox-styles) to use. |
| containerID       | string  | 'map'                                 | ID of div that will contain the map.                                    |

## Dependencies

"mapbox-gl": "^1.12.0",

"vue": "^2.6.11",

"vuetify": "^2.3.14"
