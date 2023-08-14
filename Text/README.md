
## Text to SVG

BambuStudio cannot import image files (like PNG, JPG, ...) directly, but it can import SVG files.
Here is one way (of many) to convert an image of text into an SVG file.

### First, compose text in any text editor

- e.g. Pages on Mac
- choose from available fonts and styles
- take a screenshot of the text (black text on white background)

### Next, convert screenshot to SVG

I use a Raspberry Pi for this.  Setup steps:
- install ImageMagick: `sudo apt install imagemagick`
- install Potrace: `sudo apt install potrace`

Given a screenshot of some text called `text.png`:
- convert to bitmap: `convert text.png text.bmp`
- convert to SVG: `potrace -s text.bmp`
- this will produce `text.svg`

