---
layout: page
title: Visualisation filters
subtitle: Options for visualising Earth Observation data
---

ObservedEarth contains a number of visualisation filters that change the appearance of the earth observation data it displays. These filters come in several forms as discussed in the following sections. Users can change the current filter by tapping on the visualisation bar icon, the bar can be dragged horizontally to reveal icons that may be hidden due to restricted screen real estate.

<sub>Visualisation selection bar</sub>
![Visualisation bar](../img/visualisation_bar.png)

## Preview image
![Preview image](../img/visualisation_previewimage.png)

The preview image is downloaded as a small JPEG image, it is intended to give a quick overview of the scene. From this the user can determined whether to keep, or remove the scene from the stack.

As the image is a simple JPEG ObservedEarth is unable to correct the data for sun elevation as is performed for all other data. Similarly users are not able to modify the different contrast levels of this preview image.


## Band combinations
The band combination visualisation filters map a different band to the red, green, and blue colour channels. The raw Digital Number (DN) based Landsat data is corrected for sun elevation based on the scenes metadata, this helps ensure the different temporal images have a consistent brightness. By default each band is then passed through a histogram equalisation process to ensure the DN values ranging from 0-65535 are mapped to a color value ranging between 0-255. The default histogram equalisation behaviour is overwritten when the user manually specifies a contrast range for a specific band.

Varying attributes are highlighted by mapping different bands to color channels. These are described in the following subsections.

### Natural color
![Natural color](../img/visualisation_naturalcolor.png)


### Vegetation
![Vegetation](../img/visualisation_vegetation.png)


### Urban
![Urban](../img/visualisation_urban.png)


### Agriculture
![Agriculture](../img/visualisation_agriculture.png)


### Water
![Water](../img/visualisation_water.png)


## Vegetation indices
![Vegetation indices](../img/visualisation_vegetationindices.png)


## Single band
![Single band](../img/visualisation_singleband.png)
