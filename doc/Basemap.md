# Basemap

We should style a basemap based on week 8 exercises using Google Maps.

## Resources

* [features that can be styled](https://developers.google.com/maps/documentation/javascript/reference?hl=en#MapTypeStyleFeatureType)
* [map options](https://developers.google.com/maps/documentation/javascript/reference?csw=1#MapOptions)
* [BicyclingLayer](https://developers.google.com/maps/documentation/javascript/examples/layer-bicycling)

## Available features types

| Constant | Description |
| :-------- | :---------- |
| administrative  | Apply the rule to administrative areas. |
| administrative.country  | Apply the rule to countries. |
| administrative.land_parcel  | Apply the rule to land parcels. |
| administrative.locality  | Apply the rule to localities. |
| administrative.neighborhood  | Apply the rule to neighborhoods. |
| administrative.province  | Apply the rule to provinces. |
| all  | Apply the rule to all selector types. |
| landscape  | Apply the rule to landscapes. |
| landscape.man_made  | Apply the rule to man made structures. |
| landscape.natural  | Apply the rule to natural features. |
| landscape.natural.landcover  | Apply the rule to landcover. |
| landscape.natural.terrain  | Apply the rule to terrain. |
| poi  | Apply the rule to points of interest. |
| poi.attraction  | Apply the rule to attractions for tourists. |
| poi.business  | Apply the rule to businesses. |
| poi.government  | Apply the rule to government buildings. |
| poi.medical  | Apply the rule to emergency services (hospitals, pharmacies, police, doctors, etc). |
| poi.park  | Apply the rule to parks. |
| poi.place_of_worship  | Apply the rule to places of worship, such as churches, temples, or mosques. |
| poi.school  | Apply the rule to schools. |
| poi.sports_complex  | Apply the rule to sports complexes. |
| road  | Apply the rule to all roads. |
| road.arterial  | Apply the rule to arterial roads. |
| road.highway  | Apply the rule to highways. |
| road.highway.controlled_access  | Apply the rule to controlled-access highways. |
| road.local  | Apply the rule to local roads. |
| transit  | Apply the rule to all transit stations and lines. |
| transit.line  | Apply the rule to transit lines. |
| transit.station  | Apply the rule to all transit stations. |
| transit.station.airport  | Apply the rule to airports. |
| transit.station.bus  | Apply the rule to bus stops. |
| transit.station.rail  | Apply the rule to rail stations. |
| water  | Apply the rule to bodies of water. |

## Simple styled map tutorial

JS from [Google's tutorial](https://developers.google.com/maps/documentation/javascript/examples/maptype-styled-simple)

```
function initMap() {
  var customMapType = new google.maps.StyledMapType([
      {
        stylers: [
          {hue: '#890000'},
          {visibility: 'simplified'},
          {gamma: 0.5},
          {weight: 0.5}
        ]
      },
      {
        elementType: 'labels',
        stylers: [{visibility: 'off'}]
      },
      {
        featureType: 'water',
        stylers: [{color: '#890000'}]
      }
    ], {
      name: 'Custom Style'
  });
  var customMapTypeId = 'custom_style';

  var map = new google.maps.Map(document.getElementById('map'), {
    zoom: 12,
    center: {lat: 40.674, lng: -73.946},  // Brooklyn.
    mapTypeControlOptions: {
      mapTypeIds: [google.maps.MapTypeId.ROADMAP, customMapTypeId]
    }
  });

  map.mapTypes.set(customMapTypeId, customMapType);
  map.setMapTypeId(customMapTypeId);
}
```

## Consider

* Emphasize known bike routes
* Deemphasize highways and anything that won't allow riders, but leave them for reference
* Strip out basic administrative things
* Strip out most business-like things; we know the businesses we want to display
* Limiting the extent and zoom levels (consider small screens)
* Ensuring choices are colorblind-friendly and otherwise accessible
