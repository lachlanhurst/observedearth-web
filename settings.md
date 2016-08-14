---
layout: page
title: Settings
---

The settings user interface is opened from the cog button in the top right of the earth view.

### Scene downloads
These settings control what data is downloaded by ObservedEarth.

![Scene downloads settings](../img/settings_scenedownload.png)

All Landsat8 scenes have an accompanying set of metadata, this contains a large amount of information such as the scenes location, elevation of the sun, timestamp, and cloud coverage. Before any image data is downloaded by ObservedEarth the total cloud coverage is checked against the *Cloud coverage threshold* specified in these settings. If a scene is found to have a higher percentage of cloud cover than the threshold it will not be downloaded or appear in the stack. A higher threshold will result in a larger number of scenes being downloaded.

A [high resolution download](../highresolution) may be triggered when the scene is cropped to a small region. Turning this option off will prevent ObservedEarth from downloading high resolution data, and will instead use lower resolution data irrespective of the crop extents.

### Export options

These options effect what is exported from ObservedEarth via the [share](../sharing) button.

![Export option settings](../img/settings_exportoptions.png)

ObservedEarth includes several textual overlays on image data, these include:
: ^
* Satellite from which the data was acquired. For version 1.0 this will always be Landsat8
* Path and row of the scene
* Timestamp of when the data was acquired

Each of these overlays can be turned on and off via these switches.

Export resolution specifies the image or video resolution of exported data. Animated GIFs do not respect this setting in order to maintain a sub-5MB file size.

### App settings

Housekeeping settings, these will not effect the general operation of ObservedEarth.

![App settings](../img/settings_appsettings.png)

ObservedEarth makes use of Google Analytics to return basic usage data to the developer. This information is valuable in identifying bugs and the most regularly used features, this information is used to best identify what development future releases should focus on. This information includes 'generic' information (eg; what buttons were pressed, what visualisations are used), ObservedEarth does not track what scenes are being viewed by users. *Users can opt out of tracking by turning this setting off*.

All files downloaded by ObservedEarth are cached to ensure the same data is not repeatedly downloaded, over time the volume of data may become quite significant. The *Clear cache* button removes all cached files freeing up space on the device, cleared files are re-downloaded if requested again by the user.
