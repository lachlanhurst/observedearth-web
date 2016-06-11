---
layout: page
title: FAQ
subtitle: Frequently Asked Questions
---

### What data is currently available?
Data is sourced from the [AWS Public Data Sets](https://aws.amazon.com/public-data-sets/landsat/) website. All Landsat8 data published through this website is available via ObservedEarth.

> All Landsat 8 scenes from 2015 are available along with a selection of cloud-free scenes from 2013 and 2014. All new Landsat 8 scenes are made available each day, often within hours of production. - AWS

Spatially this data covers all land areas of the Earth, including neighbouring sea areas.

Scenes from 2016 are also available.

### Will other data sources be added?
Hopefully. This requires both development time, and open access to other data sources that provide data in a raw (eg; GeoTiff) format. Landsat7 with its 15 year history, is something I would certainly like to include.

### What devices are supported?
ObservedEarth makes use of Apple's Metal API for rendering and compute functions. Much of the image processing performed would not be possible without GPU acceleration. Unfortunately this means some older iPhone and iPad devices are not supported.

The current list of supported devices includes:
: ^
* iPhone: 5s, 6, 6 Plus, 6s, 6s Plus, SE
* iPad: mini 2, mini 3, mini 4, Air, Air 2, Pro (9.7in and 12.9in)
* iPod touch (6th generation)
