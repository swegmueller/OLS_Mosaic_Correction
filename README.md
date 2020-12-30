# OLS_Mosaic_correction
This is the code to run the orthogonal least squares regression that was used as a comparison to the performance
of the LOESS Radiometric Correction for Contiguous Scenes (LORACCS). 

The paper corresponding to this work is pending publication in the open source International 
Journal of Applied Earth Observations and Geoinformation. The link will be pasted
here when available.

LORACCS was developed to create seamless mosaics using Planet Dove imagery from the same day, 
though it should work with other image sources.  It is mostly beneficial when trying to mosaic
images from different Dove satellites. The scenes should overlap, and the overlapping area should
be representative of the full scene  (for example, if the image is mostly forest, the overlap area
should have a lot of forest).

OLS works in a similar manner, but instead of correcting the image using the LOESS algorithm, 
it uses OLS.  There may be times when this method works better, so the code is being made available.

# Installation
OLS was formatted as a python class, and can be run by simply importing the class.  

The required packages are provided in the requirments.txt found in this repository. 

Note: the requirements.txt will allow you to run both the OLS and LORACCS methods.

# Usage example (using jupyter notebook or similar) 

```
from OLS_image_normalization import OLS_Image_Normalization

outdir = 'the filepath of the directory to which you would like the corrected image and associated outputs saved'
ref_img_fp = 'the filepath of the image to be used as reference'
tgt_img_fp = 'the filepath of the image to be corrected'

OLS_Image_Normalization(outdir, ref_img_fp, tgt_img_fp)
```
