---
layout: post
title:  "How To: Create a stacked raster file with Python"
date:   2015-12-10 10:11:10 +0200
categories: jekyll update

---

A stacked raster file, or raster stack, is a collection of raster layers with the same spatial extent and resolution. Since RGB visualizations in many GIS software need stacked raster images, this howto shows how to stack several raster files to a single raster stack. For this task we will use Python and especially the external [Rasterio](https://github.com/mapbox/rasterio) library. For this example I downloaded a Landsat 8 scene (LC819202820160604) and will stack the blue, green, red, NIR, SWIR 1, and SWIR 2 bands to a single raster file.

Rasterio is a very handy wrapper for the main functionalities of [GDAL](http://www.gdal.org/) for Python. Especially, the reading, writing and manipulation of raster data is extremly productive with the usage of Rasterio. 

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

Since I want to create a raster stack for the the following bands: blue, green, red, NIR, SWIR 1, and SWIR 2, I create a list variable storing all files according to the bands I wanted to stack. If you don't know the band designation just check it [here](http://landsat.usgs.gov/band_designations_landsat_satellites.php). However, I already know, that the bands I will stack are have the numbering from 2 to 7 and, hence, I search for all files in the directory ending with `B + band_number + .TIF`. The files I will append to a list which I already created out site the loop. Finally, I sort the strings in the list.

```python
raster_list = []
for name in glob.glob(raster_root_path + "/*B[2-7].TIF"):
    raster_list.append(name)

raster_list = sorted(raster_list)
```

In the next step, I iterate over all files in the `raster_list` list. For each iteration I open the file and read out the properties. I'm going to need this information for the creation of a new raster file. However, most importantly I read the raster as a multidimensional array and append it into a `band` list variable. This list was initialized outside the loop.

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



```python
ras_out = os.path.join(raster_root_path, "stack.tif")
```

```python
# create the new GTiff raster, where all array objects will be stored as
# separated raster bands
with rio.open(ras_out,
              'w',
              width=width,
              height=height,
              driver=driver,
              crs=crs,
              affine=affine,
              count=(len(bands)+1),   
              dtype=dtype,
              nodata=0
              ) as dst:
    # iterate over the bands list and write them as band to the GTiff file
    for i, b in enumerate(bands):
        dst.write(b, i+1)
```

Finally, we can open the stack.tif file in QGIS. For the figure below I selected a false color visualization with the band combination: NIR, Red, and Green. This combination, is very helpfull for the visual interpretation of vegetation. 



![Stack in QGIS](/assets/rasterstack/QGIS.png)

