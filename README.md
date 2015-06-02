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

## Options
- `url` URL of the Photon API to use. *Default: 'http://photon.komoot.de/api/?'*
- `placeholder` Placeholder of the search input. *Default: "Start typing..."*
- `noResultLabel` Message to display when no result has been found. *Default: "No result"*
- `minChar` Min char to be typed before actually searching (can be a function that
   takes the val as parameter and must return a boolean). *Default: 3*
- `limit` Number of results max to return from API. *Default: 5*
- `submitDelay` Min time buffer between to sent request, to avoid too much
  requests when typing fast (in milliseconds). *Default: 300*
- `includePosition` Whether to include or not the map center as location bias
  for the search. *Default: true*
- `feedbackEmail` Email to use as feedback link. Set to null to disable the
  feedback box. *Default: "photon@komoot.de"*
- `feedbackLabel` Message for feedback link. *Default: "Feedback"*
- `lang` land code (en, it, fr…) to send to Photon API. *Default: null*
- `onSelected` Action to run when user select a search result. *Default: center
  map on selected result's latlng*
- `formatResult` Optional function to control the way geojson features are
  displayed in the results box.
- `formatType` Optional function to control the way features types (amenity,
  school, etc.) are displayed in the default `formatResult` function.
- `resultsHandler` Optional function that will be called when a geojson is
  retrieved from the API. You way want to use this to display points in the map
  for instance.


## Events
- `focus` sent on input focus
- `blur` sent on input blur
- `hide` sent on result box hide
- `selected` sent on result select. Event: {choice: <selected geojson feature>}
- `ajax:send` sent when an ajax call is made
- `ajax:return` sent when an ajax call is returned
