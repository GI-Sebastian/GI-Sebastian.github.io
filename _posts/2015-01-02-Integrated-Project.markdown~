---
layout: post
title:  "Dwelling extraction in a refugee camp"
date:   2015-01-02 18:15:40 +0200
categories: jekyll update
---
During my study in Salzburg [Pascal Krafft](http://pascalkrafft.xyz/) and I worked together on a project for the automatic extraction of dwellings in refugee camps. We decided to create a ArcGIS toolbox, so that also other users can adapt this approach to their studies. The following post shows the motivation, workflow, and the results for our developed toolbox. The toolbox was tested for the Lukole refugee camp. Additionally, we created a poster which you can [get as PDF here](/downloads/Poster_Krafft_Scheckel.pdf).

## Motivation
 
Every year thousands of people have to leave their homes due to famines, wars or natural crisis like earthquakes, flooding, or hurricanes. Often the only shelter that they can find are refugee camps which are built by humanitarian organizations.

Due to fast response to a humanitarian crisis refugee camps run the risk that the structure of such camps can have a high complexity. Therefore we try to help the decision makers in such camps.
With our toolbox the users can analyze and extract the number of dwelling in a refugee camp. Hence the decision-makers can extract the camp borders, calculate density maps of the dwellings, and extract statistical key data of the camp.

Our main aim of this project is to build an easy-to-use OBIA-Toolbox for ArcGIS in order to extract and analyze dwellings in refugee camps. This toolbox has to fulfill those three objective:

1. Implement different segmentation algorithms.
2. To be able to filter the objects from the segmentation step.
3. Calculate basic statistics about the segments.

In the following project report we will present the basic workflow of our toolbox as well as the different tools which are implemented. Also a help menu was included to the tools. 


## Workflow 

Since most object-based image analysis methods are separated into two steps, we also implemented this approach to our toolbox. Therefore, we have tools for the segmentation and tools for the object analysis and filtering. Furthermore, we created some output tools in order to produce a density raster, camp border polygon, and statistical key data. A graphic illustration of the basic tool workflow can be seen in the figure below.

![Description of the workflow](/assets/IP/workflow.png)

At first the user needs to have some image raster data. Some tools only work with stacked raster other with single band raster data.

The Segmentation tools work with the raster data and are able to segment the image into meaning-full objects based on a histogram threshold segmentation according to the distribution of the raster values from the images. The segments will be saved as a vector file (i.e. shapefile).

In the next step the vectorised segments can be transferred to the Object tools. Firstly the Shape Area and Shape Index will be calculated and added to the attribute table for each segmented polygon. This step is necessary in order to filter and identify unclear objects based on the attribute values. Afterwards from the filtered segmentation layer the output tools can calculate the result data mentioned above.

As a side product we also implemented the Index Calculator tool which can be used in order to help to find the fitting threshold value for the Index Threshold tool.



## Lukole 

In the north-west of the United Republic of Tanzania the refugee camp is situated. It is close to the Rwanda and Burundi border and was erected in order to give refugees that fled due to ethnical and political riots. The camp was managed by the United Nations High Commissioner for Refugees (UNHCR) and was erected in the year 1994. The maximum population the camp had was in the year 2000 with more than 129,000 people. The number of inhabitants declined since then.


![Area of interest](/assets/IP/aoi.png)

Due to the high population in the camp this had in high impact on the environment. Many trees were cut and used as timber for construction as well as firewood for cooking. In order to limit the damages on the surrounding forest in 2006 reparation processes were started. The results of this processes is that in the year 2013 almost the whole camp area was covered by trees while most dwellings had been dismantled.

## Data 

For this project two images and the panchromatic images belonging to them from two different sensors with different spatial resolution were used. Also different acquisition years were used. The image from 2000 is an IKONOS scene, which was pan-sharpened to a ground sample distance of 1.0m. The image from 2005 is a QuickBird scene, pan-sharpened to a ground sample distance of 0.6m.



## Results 

The aims to dismantle the camp and simultaneously to reforest in order to reduce the ecological footprint accrued by the residents are reflected in the results. The camp area was reduced from 12.7 km² in 2000 to 6.3 km² in 2005. Moreover the number of the dwellings is also reduced from ~24,000 to ~4,600. By applying the estimated occupancy rates between 5 and 6 people per tent, depending on coming and going waves of refugees. There would live in the year 2000 about 115,000 to 144,000 people and in 2005 about 23,000 to 27,000. Three months after the image was taken in 2000 there were counted more than 129,000 persons in the camp. Therefore our dwelling extraction is quite fitting. A density raster of the dwellings for both years is presented the figure below combined with a diagram showing the distribution of the dwelling size. The density layer illustrats really good where the hot spots of the huts are located.

![Description of the workflow](/assets/IP/result_1.png)

Furthermore, the wrong colored image for each year is presented. There it is not only an impression that the vegetation is thicker in 2005 compared to 2000 also the extracted vegetation mask supports this assumption. In the year 2000 about 38% of the camp area were covered by vegetation. In the year 2005 about 73% of the camp region of 2000. These numbers cannot be directly compared because the images were taken at different seasons.


![Description of the workflow](/assets/IP/result_2.png)






















