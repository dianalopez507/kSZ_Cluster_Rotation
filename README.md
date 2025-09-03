# Description
Jupyter notebook compiling results of the Research Project: Searching for signature of galaxy cluster rotation using ACT data.

# Content
## Test: Dipole signal
Generate a 2D map with a circle of a defined radius. Inside the circle, one half is +vmax and the other half is -vmin. White Gaussian noise with RMS 'noise_sigma' is added to the full map. The 2D maps are added to the cuouts from DR6 CMB temperature maps. The circle is oriented in an angle given as a parameter (projected axis of rotation). The output is a fits file with the original WCS information.

## Rotation
Rotates a simple 2D FITS image and its WCS information.
Modification of: https://gist.github.com/dsberry/4171277 (credit: David Berry, East Asian Observatory) 

## Cropping
Extract a smaller cutout of the maps, given its physical size (Mpc) or R500 parameter.

## Flipping
Flips the maps horizontally according to n_flip parameter (int). 

## Repixelation
Repixelate the maps into a common grid image of shape_to_resize*shape_to_resize in pixels.

## Mean substraction and masking
Masking: set as np.nan the 0 values if presents. Mostly due to residual parts of the rotation and cropping.
Mean substraction: subtract the mean value of the maps with masked values.

## Stacking
Stack n maps and write the result as a fits file. 
