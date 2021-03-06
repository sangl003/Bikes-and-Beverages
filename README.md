# GIS-5574: Bikes and Beverages

Intelligent routing for bike-brewery/bike-distillery tours of the Twin
Cities using on-sale and off-sale liquor license data and simulated
annealing for maybe-optimal route determination. Random routes, route
suggestions based on distance criteria, and customizable routes are
provided.

## Purpose

You like to bike. You're a discriminating consumer of craft beer and
spirits. You enjoy mixing the two. You go into a day (or night)
thinking to yourself, "I want to visit five taprooms today." Or, maybe,
"I'd like to bike about 30 miles and visit 2-4 taprooms or distilleries."

## Extensibility

You can easily extend this to include arbitrary place-types (e.g.,
maybe you want to visit various libraries in the Twin Cities); no
assumptions are made about destinations, other than that they can
be placed in one or more groups and that destinations are selected
based on group membership.

## Data sources

* Minneapolis OpenData has [on-sale](http://opendata.minneapolismn.gov/datasets/8c97cfb0700b4c8b929459dc5744efc3_0) and [off-sale license data](http://opendata.minneapolismn.gov/datasets/a0448b7b87f04899822478467f6830db_0)
* [Minnesota Craft Brewers Guild](http://www.mncraftbrew.org/) has a [set of markers](http://www.mncraftbrew.org/wp-content/plugins/store-locator/sl-xml.php)
* St. Paul doesn't have data available online; email sent to request

## Web services

Mostly-reliant on Google APIs (routing), but may make use of OSM+Leaflet
or other mapping services.

## Disclaimer

You are responsible for yourself. Reliance on this software and/or
any of the data used may result in just about anything, including
horrific bodily harm or death. You assume all risks and
responsibilities. Bike carefully. Drink carefully. Be safe.
