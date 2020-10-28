# Change sublayer renderer

Apply a renderer to a sublayer.

![Image of change sublayer renderer](ChangeSublayerRenderer.png)

## Use case

A layer showing animal populations contains sublayers for different species. A renderer could be applied which gives each sublayer a different color, so that populations of each species can be compared visually.


## How it works

1. Create an `ArcGISMapImageLayer` from its URL.
2. After it is done loading, get its `SublayerList` with `imageLayer.getSublayers()`.
3. Cast the sublayer you want to change to the appropriate type: `(ArcGISMapImageSublayer) sublayers.get(0)`.
4. Create a `ClassBreaksRenderer` with a collection of `ClassBreak`s for different population ranges.
5. Set the renderer of the sublayer with `sublayer.setRenderer(renderer)`.

## Relevant API

* ArcGISMapImageSubLayer
* ClassBreaksRenderer
* ClassBreaksRenderer

## Tags

class breaks, dynamic layer, dynamic rendering, renderer, sublayer, symbology, visualization

## About the data
This application displays census data from an ArcGIS Server map service. It contains various population statistics, including total population for each county in 2007.

## Additional information
The service hosting the layer must support dynamic layers to be able to change the rendering of sublayers.

## Offline data

This should be allowed. 

## Not an optional section

This section should not be be allowed. 
