# SVG

## Position
### The grid
* Similar to `canvas`, top left corner is (0, 0)
* Positions are then measured in `pixels` from the top left corner, 
with the positive x direction being to the right, and the positive y direction being to the bottom.

### What are 'Pixels'
* In most case, one pixel in svg document maps to one pixel on output device(the screen)
* But SVG is `scalable`, SVG defines absolute units and so-called `user unit`, that lack that identifier and are plain numbers.
* Without further specification, one user unit equals to one screen unit(one pixel)
* There are several ways to change this behaviour

``` html
<svg width="100" height="100">
```
The above element defines a simple SVG canvas with 100x100px, One user unit equals one screen unit.

``` html
<svg width="200" height="200" viewBox="0 0 100 100">
```
The whole SVG canvas here is 200px by 200px in size. 
However, the viewBox attribute defines the `portion` of that canvas to display. 
These 200x200 pixels display an area that starts at user unit (0,0) and spans 100x100 user units to the right and to the bottom. 
This effectively zooms in on the 100x100 unit area and enlarges the image to double size.


The current `mapping` (for a single element or the whole image) of `user units to screen units` is called `user coordinate system`.
The default user coordinate system maps one user pixel to one device pixel.



