<template>
<div class="map-container">
    <div class="map-text">
        <h2>Hof van Cartesius</h2>
        <p>Vlampijpstraat 84, 3534 AR Utrecht</p>
    </div>
    <div class="map" id="map"></div>
</div>
</template>

<script>
var mapboxgl = require('mapbox-gl/dist/mapbox-gl.js');

const lat = 5.085049;
const long = 52.1047128;

const coordinates = [lat, long];

export default {
    name: 'map',
    mounted: function() {

        mapboxgl.accessToken = 'pk.eyJ1IjoidG9tb290ZXMiLCJhIjoiOXRKWGVCUSJ9.QaSlGLJBy4CE2nDNpe-OLg';
        var map = new mapboxgl.Map({
            container: 'map',
            style: 'mapbox://styles/mapbox/light-v9',
            center: coordinates,
            zoom: 13
        });

        var geojson = {
            type: 'FeatureCollection',
            features: [{
                type: 'Feature',
                geometry: {
                    type: 'Point',
                    coordinates: coordinates
                },
                properties: {
                    title: 'Kantoor Ootes Web',
                    description: ''
                }
            }]
        };

        // add markers to map
        geojson.features.forEach(function(marker) {

            // create a HTML element for each feature
            var el = document.createElement('div');
            el.className = 'marker';

            // make a marker for each feature and add to the map
            new mapboxgl.Marker(el)
                .setLngLat(marker.geometry.coordinates)
                .setPopup(new mapboxgl.Popup({
                        offset: 25
                    }) // add popups
                    .setHTML('<h4>' + marker.properties.title + '</h4><p>' + marker.properties.description + '</p>'))
                .addTo(map);
        });

		map.scrollZoom.disable();



    }
}
</script>
