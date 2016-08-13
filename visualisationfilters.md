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

The natural color visualisation is a direct mapping of the red, green, and blue (4, 3, 2) bands to the displayed images RGB color chanels. This displays the data as close as possible to what would be observed from space.

The *Preview image* is generated in a similar manner. The difference is that this visualisation is based on the raw data allowing it to be is corrected for sun elevation helping even the brigthness across time. The contrast can also be manually modified within ObservedEarth to show detail that may be washed out, or over/under-saturated in the preview image.

### Vegetation
![Vegetation](../img/visualisation_vegetation.png)

For the Vegetation filter the Near Infra-Red (NIR) band 5 is mapped to the red colour channel. Healthly vegetation reflects more light in the NIR spectrum, therefore regions of vegetation are highlighted in bright red when using this visualisation. 

Bands 5, 4, and 3 are mapped to the RGB color channels in this visualisation.


### Urban
![Urban](../img/visualisation_urban.png)

Urban regions, or ground with harder surfaces are highlighted in purple when using this visualisation.

Band 7, the mid infrared band, is mapped to the red color channel. As this band picks up active heat sources it is useful in picking up bushfires and other sources of heat.

Bands 7, 6, and 4 are mapped to the RGB color channels in this visualisation.

### Agriculture
![Agriculture](../img/visualisation_agriculture.png)

This visualisation helps differentiate argiculture from other types of vegetation. Crops will appear as bright green, whereas other plant life will have a darker shade.

Bands 6, 5, and 2 are mapped to the RGB color channels in this visualisation.

### Water
![Water](../img/visualisation_water.png)

Bands 5, 6, and 4 are mapped to the RGB color channels in this visualisation.


## Vegetation indices
![Vegetation indices](../img/visualisation_vegetationindices.png)

The following vegetation indices are included in ObservedEarth:
: ^
* Normalized Difference Vegetation Index (NDVI)
* Soil Adjusted Vegetation Index (SAVI)
* Enhanced Vegetation Index (EVI)

These indices are described in the [*Landsat Surface Reflectance-Dervived Spectral Indices - Product Guide*](http://landsat.usgs.gov/documents/si_product_guide.pdf) produced by the United States Geological Survey.

    NDVI = (Band 5 – Band 4) / (Band 5 + Band 4)
    
    SAVI = (Band 5 – Band 4) / (Band 5 + Band 4 + 0.5) * 1.5
    
    EVI = (Band 5 – Band 4) / (Band 5 + 6 * Band 4 – 7.5 * Band 2 + 1)

All three indices range between -1 and 1, higher values indicate vegetation, whereas values below 0 indicate no vegetation. The index value for each pixel is mapped to a color via a lookup table; values below -0.2 are black, values near zero dark blue, and from 0 though 1 colours transition from red to green. Green indicating regions of lush vegetation.

ObservedEarth calculates to Top of Atmosphere (ToA) reflectance using the sun elevation extracted from the scenes metadata. The value for each band is then fed into the above equations. As of version 1.0 it is not possible to adjust the contrast of these indices.

## Single band
![Single band](../img/visualisation_singleband.png)

Data for each of the 9 Landsat8 bands can be displayed individually using these filters. DN values are corrected for sun elevation and then by default passed through a histogram equalisation process to convert to a value between 0 and 1. By specifying a contrast range the default histogram equalisation is overwritten. Low values are shown in blue, higher values red.

Contrast ranges are specified on a per band basis, and these are carried over across visualisations. It is often easier to modify contrast ranges for a band combination visualisation one band at a time using the single band visualisation.