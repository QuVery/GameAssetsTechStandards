# UI

## Single Color Images

Images that have only one color are produced in white and the color code is set inside the engine. For example, UI buttons that have a fixed color.

## 9-Slice Images

9-slice scaling (also known as Scale 9 grid, 9-slicing or 9-patch) is a 2D image resizing technique to proportionally scale an image by splitting it in a grid of nine parts.

In most cases, when we need a uniform template for multiple sections and the only difference between these sections is their dimensions, we produce images that can be divided into 9 parts. 

5 middle parts (left, right, top, bottom and center) are stretched in different dimensions and 4 corner parts (top-left, top-right, bottom-left and bottom-right) always have the same size. With this method, we can use a fixed image for different dimensions of buttons, panels, progress bars and other sections.

[More info](https://en.wikipedia.org/wiki/9-slice_scaling)