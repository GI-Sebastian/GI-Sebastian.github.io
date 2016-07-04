---
layout: post
title:  "How To: Create a stacked raster file with Python"
date:   2015-12-10 10:11:10 +0200
categories: jekyll update

---

A stacked raster file, or raster stack, is a collection of raster layers with the same spatial extent and resolution. Since RGB visualizations in many GIS software need stacked raster images, this post shows how to stack several raster files to a single raster stack. For this task we'll use Python and especially the external [Rasterio](https://github.com/mapbox/rasterio) library. For this example, I downloaded a Landsat 8 scene (LC819202820160604) and I will stack the blue, green, red, NIR, SWIR 1, and SWIR 2 bands to a single raster file.

Rasterio is a very handy wrapper for the main functionalities of [GDAL](http://www.gdal.org/) for Python. Especially, the reading, writing and manipulation of raster data is extremly productive and simple with Rasterio. 

In the first step, I'll need to import the Rasterio package into my Python file. Additionally, I import the build in libraries `glob` and `os`. The `os` library profides functionalities of the operating system. With `glob` it is possible to use Unix style pathname patterns.

```python
import glob
import os
import rasterio as rio
```

In the next step, I create a variable pointing to the directory where the GeoTiff files of the Landsat 8 are located. To concatenate a path string I use the `path.join` method provided by the `os` library.

```python
raster_path = os.path.join(os.sep, "home", "sebastian, "Documents", "Data", "LC819202820160604")
```

Since I want to create a raster stack for the the following bands: blue, green, red, NIR, SWIR 1, and SWIR 2, I create a list variable storing all files according to the bands I wanted to stack. If you don't know the band designation just check it [here](http://landsat.usgs.gov/band_designations_landsat_satellites.php). However, I already know, that the bands I want to stack have the numbering from 2 to 7. Since the naming of all raster files for Landsat 8 have the same schema, I search for all files in the directory ending with "`B[2-7].TIF`". The files will be appended to a list created already outsite the loop. Finally, the strings in the list are sorted.

```python
raster_list = []
for name in glob.glob(raster_root_path + "/*B[2-7].TIF"):
    raster_list.append(name)

raster_list = sorted(raster_list)
```

In the next step, I iterate over all files in the `raster_list` list. For each iteration I open the file and read out the properties. I'm going to need this information for the creation of a new raster file. However, most importantly I read the raster as a multidimensional array and append it into a `band` list variable. This list had been initialized outside the loop.

```python
bands = []
for b in raster_list:
    with rio.open(b) as src:
        width = src.width
        height = src.height
        driver = src.driver
        crs = src.crs
        affine = src.affine
        array = src.read(1)
        dtype = array.dtype

        bands.append(array)
```

The raster stack also needs a output GeoTiff file. Usually, you should use a more descriptive name then the one used in this example. I recommend to concatenate the scene ID by the band numbers stacked in the file. In this case `LC819202820160604_B765432.tif` would be a long but descriptive name. 

```python
ras_out = os.path.join(raster_root_path, "stack.tif")
```

The output GeoTiff file is opened with `rasterio` and all properties read out from the initial raster files are stored to the new raster files. Additionally, the count of raster band is set to the length of the band array list and the `nodata` value is set to `0`. With a for-each loop the arrays from the `bands` list are writen to the raster file. The `bands` list is looped and with the `enumerate` function a counter variable is created. The counter variable is needed for the definition to which band the according array will be stored. Because Python indices are zero based the counter must be alterated by +1.



```python
with rio.open(ras_out,
              'w',
              width=width,
              height=height,
              driver=driver,
              crs=crs,
              affine=affine,
              count=len(bands),   
              dtype=dtype,
              nodata=0
              ) as dst:
    for i, b in enumerate(bands):
        dst.write(b, i+1)
```

Finally, we can open the stack.tif file in QGIS. For the figure below I selected a false color visualization with the band combination: NIR, Red, and Green. This combination, is very helpfull for the visual interpretation of vegetation. 



![Stack in QGIS](/assets/rasterstack/QGIS.png)

