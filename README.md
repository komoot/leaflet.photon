leaflet.photon
==============


Smaple Usage

```javascript
function myHandler(geojson) {
    console.debug(geojson);
}
var map = L.map('map', {
  photonControl: true,
  photonControlOptions: {
      resultsHandler: myHandler,
      placeholder: 'Try me …',
      position: 'topleft'}
  }
);
```
