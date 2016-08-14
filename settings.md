---
layout: page
title: Settings
---

The settings user interface is opened from the cog button in the top right of the earth view.

### Scene downloads
These settings control what data is downloaded by ObservedEarth.

![Scene downloads settings](../img/settings_scenedownload.png)

All Landsat8 scenes have an accompanying set of metadata, this contains a large amount of information such as the scenes location, elevation of the sun, timestamp, and cloud coverage. Before any image data is downloaded by ObservedEarth the total cloud coverage is checked against the *Cloud coverage threshold* specified in these settings. If a scene is found to have a higher percentage of cloud cover than the threshold it will not be downloaded or appear in the stack. A higher threshold will result in a larger number of scenes being downloaded.

A [high resolution download](../highresolution) may be triggered when the scene is cropped to a small region. Turning this option off will prevent ObservedEarth from downloading high resolution data, and will instead crop the lower resolution data irrespective of the crop extents.

### Export options


![Export option settings](../img/settings_exportoptions.png)


### App settings


![App settings](../img/settings_appsettings.png)


* what each setting does
