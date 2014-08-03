leaflet.photon
==============

This is [leaflet](http://leafletjs.com/) plugin for [photon](https://github.com/komoot/photon/).

## Sample Usage

```javascript
function myHandler(geojson) {
    console.debug(geojson);
};

var map = L.map('map', {
  photonControl: true,
  photonControlOptions: {
      resultsHandler: myHandler,
      placeholder: 'Try me …',
      position: 'topleft'}
  }
);
```
