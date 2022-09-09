pstools
=======

A collection of utilities handy for develloping for the PicoSystem API.

These are all standalone python scripts, so you should be able to install them wherever you 
would normally stick such things.

pst_image.py
------------

Generates header files for images, in an appropriate format for use as spritesheets or blit
operations.

This does a similar job to the excellent online tool on the 
[PicoSystem wiki](http://wiki.picosystem.com/en/tools/image-converter), but with a couple of
crucial default differences

* it generates both the raw image data (a `color_t` array named `<imagename>_data`)
* it declares this as `const`, so that the data isn't loaded into RAM, allowing for larger
  spritesheets
* it declares an appropriate `buffer_t` structure (named `<imagename>_buffer`) that can be
  passed directly to `spritesheet()` or `blit()`

