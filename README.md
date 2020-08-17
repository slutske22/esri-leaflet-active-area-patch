# esri-leaflet-active-area-patch

### What is this?
When using [esri-leaflet](https://esri.github.io/esri-leaflet/) with [leaflet-active-area](https://github.com/Mappy/Leaflet-active-area), any derivative of L.esri.RasterLayer becomes distorted when added to a map with an activearea.  Take the following example, where a `dynamicMapLayer` is added to a map that has an active area applied (outlined in dotted blue):

![the problem](/esri-leaflet-activearea-1.PNG)

The layer is distorted, as it us using the bounds of the entire map to retrieve the image, but then the image is applied to the bounds of the active area.  Enter `esri-leaflet-active-area-patch`:

![the solution](/esri-leaflet-activearea-2.PNG)

Voila!  Fixed.

### Install and Use

````javascript
npm install esri-leaflet-active-area-patch
````

And somewhere in your project:

````javascript
import 'esri-leaflet-active-area-patch'
````

And that's it!  Enjoy.
