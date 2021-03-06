---
layout: post
title:  "Spatial Optimization"
date:   2015-05-15 10:11:10 +0200
categories: jekyll update

---

Spatial optimization is a concept which in general is used by everyone and everyday. But most people are not aware that they apply those concepts in their daily life. In fact, humanity wasn’t aware of spatial optimization in an academic meaning a long time. What is certain, however, that spatial optimization techniques had been applied since prehistoric times.

But what is spatial optimization and why is it such an important concept for our daily life? A short and easy definition of the concept of spatial optimization can be found in Church (2001): ”...[spatial optimization] involves identifying how land use and activities should be allocated and arranged spatially in order to optimize efficiency or some other measure of goodness.” (Church 2001, 14811)

When we apply this abstract and general definition to a concrete real problem, we see that we all are effected by spatial optimization concepts. Imagine a city with several elementary school. With increasing urbanization of the city region the number of population as well as the birthrate will increase. As a result of this development the demand for new elementary schools will emerge. But where should they be located in order to reach most students?

Hence, we see that spatial optimization can help us to solve this problem. We have a optimization problem (reach a high number of students) and in order to solve this problem the spatial context is crucial (location of new schools). Thus, we see the connection between the abstract definition and the concrete example.

Starting from this example, dozens or hundreds of similar spatial optimization problems can be imagine. Just by simply changing the subject schools, to retail shops or fire departments  the questioners will also be different. While economic geographers will be more interested in the best position for a retail shop, city planers will be more interested in the best position of a fire department. Therefore, a lot of academic disciplines have to deal with spatial optimization. And even more academic fields could profit from spatial optimization but might not be aware of this concept.

Since most spatial optimization techniques are based on geographic concepts, the discipline of Geography profits and contributes a lot. And so do adjacent disciplines. It should be easy to image scenarios where fields like geology, forestry, biology, ecology, transport engineering, or GIScience can benefit from different spatial optimization problems (just to mention a few academic disciplines)

With the acquisition of more and more detailed spatial data, favorable computational power, improving graphics, and advances in geographic information systems and techniques (GIS & T) the use of spatial optimization increases. With the growing demand the need for contributing sciences towards spatial optimization is required.

Geography is one of those disciplines contributing to spatial optimization. And also the other academic fields are involved developing advanced spatial optimization techniques. Usually, in order to answer a research question in their related fields.

The advances in GIS & T increases the use of spatial optimization, as previously said. Then again with GIScience standing behind the technology and system, this academic discipline seems more involved in the contribution towards spatial optimization. Hence, it seems reasonable that spatial optimization is an important subfield of GIScience. But according to (Tong and Murray 2012) spatial optimization has long been a relevant subspeciality of Geography.

## History of Spatial Optimization

Everyone is facing some spatial optimization problem everyday. For example if we travel from our living place to our workplace by bicycle we use spatial optimization techniques in order to drive the shortest path. Therefore it can be expected that spatial optimization is old as mankind (Church 2001, Tong and Murray 2012).

For hunter-gatherers societies the basic concepts were essential for their survival. Finding the best place for a trap or the best location to fish, are only two examples where optimization was crucial. And with the development of settled communities spatial optimization gained more importance (Church 2001).

In order to study such prehistoric settlements and settlement patterns archaeologists, anthropologists, and geographers have analysed these early societies according to different spatial optimization techniques (Church 2001, Church and Bell 1988, Reidhead 1979). And even in the ancient Feng-Shui art spatial optimization concepts can be recognized (Church 2001).

The first time spatial optimization was clearly described in a publication was in 1826 with the work of von Thunen. He explained how an isolated village should locate their surrounding agricultural activities in order to optimize the land rent between different field crops (Church 2001, Tong and Murray 2012, Von Thunen 1826).

The work of Alfred Weber in 1908 examined industrial location models for cost minimization (Weber 1908). Figure 1 shows a simple example of the classic triangle plotted in a Cartesian coordinate system used by Weber. It describes where a manufacturing facility should be located in order to optimize the transportation distances. The two points for the raw material an the one point for the market can be plotted as an triangle in a Cartesian coordinate system. With the assumption that the distances are Euclidean the ideal location for the facility can be calculated (Church 2001, Weber 1908).

![WEBER Triangluation solution](/assets/spatialoptimization/triangulation.png)

In 1933 Walter Christaller searched for certain geographic laws that determine how towns in Southern Germany are arranged (Christaller 1966). He counted the number of telephone connections and hierarchically grouped the towns into major (regional) centers, mid-sized centers, and sub-centers. This central place theory is still used by archaeologists, anthropologists, and geographers in order to find similar patterns in different regions (Church 2001).

With advances in linear programming during the 1950s the use of spatial optimization in order to study geographic phenomena increased (Tong and Murray 2012). In 1959 one of the first explicit optimization problem with spatial issues was published by Garrison (Garrison 1959). Haggett in 1975 made the first publication where spatial optimization was included in a clearly geographic publication (Haggett 1975). Since then the number of spatial optimization publications tend to increase. This development is not only noticeable in the academic fields of Geography, but also in transportation, forestry, ecology, and since 1992 also in GIScience (Tong and Murray 2012).

## What is a Spatial Optimization Problem?

According to Tong and Murray (2012) in order to formulate a spatial optimization problem, three components, similar to engineering or mathematics, can be named:

1. an Objective
2. Decisions to be made
3. constraining Conditions

All components will be explained with the example of a fictive area which should be monitored by using a sensor network (see figure 2). The red dots show the potential location for the sensors and the black rectangle represents the area of interest, which will be monitored.

![Sensor Location](/assets/spatialoptimization/sensor.png)

The objective of a spatial optimization problem, like every other problem, is it to reach a certain goal. In our example it is to monitor the whole area of interest (see figure 2 the black rectangle). Therefore the objective can have different formulations always according to the problem. Mostly the goals to be achieved are to minimize costs or to maximize profits. Different scenarios would also include to minimize the costs when a pipeline corridor is planned or to locate a retail store in order to maximize the accessibility and thus the profit (Tong and Murray 2012).

The decisions to be made can also referred as decision variables (Tong and Murray 2012). In figure 2 the different decisions are represented by the symbols X 1 ...X 12 . This means that on every position with a red dot a possible location for a sensor is situated.

The constraining conditions are the limitations of a certain problem (Tong and Murray 2012). For the sensor network example, a possible limitation might be that only five sensors are affordable due to a limited budget. Also different possibilities of limitations can be represented by restrictions of the locations of the sensor. For example when a potential sensor location is not accessible.

## Concepts of Spatial Optimization

According to Nystuen (1968) distance is one of the most fundamental spatial concepts. Also the first law of Geography, formulated by Walter Tobler (1970), refers to similarities between objects as a function of proximity. Furthermore it is irrelevant for this concepts if the traveling distance or traveling time are described.

![distance](/assets/spatialoptimization/distance.png)

Distance can be measured in different ways. Usually for a 2-dimensional room Euclidean or network distances are used (see figure 3). Because the technical aspects of more advanced distance measures which are used in a 3-dimensional room would go beyond the scope of this work, detailed descriptions can be found in Church and Murray (2009), Miller and Wentz (2003), and de Smith et al. (2007).

The concept of distance can be implemented in a spatial optimization problem as a function or constraining conditions. Also distance can be used as a model coeffizient (Tong and Murray 2012).

In the work of Alfred Weber (1908) also Euclidean distance is used as a function, in order to find the optimal location for the manufacturing facility. Furthermore also Von Thunen (1826) used distance as a coefficient in his studies.

Noted spatial optimization problems, where distance is crucial, include the simple plant location problem (Love et al. 1988), the p-Median location problem (ReVelle and Swain 1970, Church 1990), among other facility or center location problems (Goodchild and Massam 1969, Oppong and Hodgson 1994, Horner and Downs 2007).

Also connectivity is according to Nystuen (1968) a fundamental spatial concept, which is often incorporated in spatial optimization problems. Connectivity means that it is possible to get from one position to another position without any hindrance (Tong and Murray 2012).

Connectivity is mostly referred in a network of paths or roads. The features of connectivity are represented as Boolean values, because two locations are connected or are not connected (Tong and Murray 2012).

In a spatial optimization problem connectivity is mostly implemented as a constraining condition. Furthermore connectivity is used as constraining conditions in the land acquisition for reserved lands or to observe if a potential facility is connected to the major road network. Furthermore connectivity is also important for constructing telecommunication networks (Tong and Murray 2012).

Noted spatial optimization problems, where the concepts of connectivity is implemented, include the land use and nature reserve planning (Williams 2002, Shirabe 2005, Wu and Murray 2008, Ligmann-Zielinska et al. 2008) and transportation networks (MacKinnon 1970, O’kelly 1987, Kim 2009).

Containment is the concept that one or more geographical objects are within another object (Longley 2011, Tong and Murray 2012). Figure 4 shows the potential location of a retail store and a distance buffer around the location. On the on hand the distance buffer zone or trade zone is the representation of the first geographic object. On the other hand the small houses represent other geographic objects. Therefore the households 1 and 2 are contained by the buffer zone, while household 3 is not contained
in the trade zone of the retail shop.

![Buffer](/assets/spatialoptimization/buffer.png)

The concept of containment is mostly implemented in spatial optimization problems as a coefficient. But it can be also included as a constraining condition (Tong and Murray 2012). For example if new locations for schools are investigated and in some districts already more than five schools existing, there is no need for a new school in this area.

Noted spatial optimization problems, where the concepts of containment is implemented,include groundwater monitoring (Hudak et al. 1993), reserve selection (Church et al. 1996), health care facility location problem (Oppong and Hodgson 1994), and emergency response planning (Bianchi and Church 1988), Sorensen and Church (2010).

Figure 5 shows the geographic concept of intersection. Intersection exists where two or more objects (partially) share the same space. Also the concepts of union, difference, and complement from the set theory come along with intersection (Longley 2011, Tong and Murray 2012).


![Intersection](/assets/spatialoptimization/intersection.png)

In a spatial optimization problem intersection is included mostly implemented as a constraining condition. Those restrictions can be implemented in a positive as well in a negative way (Tong and Murray 2012).

An example for a positive implementation of intersection as a constraining conditions would be the location planning of fire departments in a town. For security issues it is important that areas in the inner city can be responded by more than one fire station. Therefore a certain degree of overlapping is needed as a positive constraining condition (Tong and Murray 2012).

An example for a negative implementation of intersection as a constraining conditions can also be found in the location planning but for retail shops. As already mentioned in the example for the concept of containment, retail shops have a trade zone. In order to optimize the location of retail shops this zones should not overlap and thus the retail shops serve different neighborhoods (Tong and Murray 2012).

Noted spatial optimization problems, where the concept of intersection is implemented, include backup coverage for location of emergency response services and medical services (Hogan and ReVelle 1986, Erdemir et al. 2010), nature reserve planing and design (Malcolm and ReVelle 2005). More recently intersection is an importan issue for coverage in security monitoring (Murray et al. 2007, Kim et al. 2008)

The spatial concept of shape has been of interest for longer time. Although the importance of shape was recognized and discussed early (Bunge 1962, Boyce and Clark 1964) it is viewed as a vague term or concept (Tong and Murray 2012).

Nevertheless shape is an important characterization for geographic objects. Often it is compared to known structures, like rectangle or circle (Tong and Murray 2012). Also formulas to calculate shape features, including shape length and shape index exists. The latter formula calculates a index within a range from zero to one. A value close to one represent a circular object, while a value close to 0 represents a horizontally split object with a structurally rich form. Nonetheless there is no general and valid definition and therefore the concept of shape is still challenging and discussed (Wentz 2000). Figure 6 shows three different forms sorted according to the shape index.


![shape](/assets/spatialoptimization/shape.png)

The concept of shape is considered many times in spatial optimization. The evaluation what type of shape is considered as positive or negative depends on the research question. For example for political questions on the one hand elongated shapes are viewed as problematic or negative, because they can be made in order to collect specific regions to one election district. On the other hand in nature reserve planning elongated shapes are viewed as positiv for animals that move in corridors (Tong and Murray 2012).

Noted spatial optimization problems, where the concept of shape is implemented, include nature reserve design (Williams and ReVelle 2004), land-use allocation (Aerts et al. 2003, Shirabe 2005) and the assessment of service areas (Goodchild and Massam 1969).

Also the spatial concept of district is also referred as a not universal term. Besides districts also the names region or partition are used. As well as the the concept of shape has longer been of interest, also the concept of district was recognized and discussed early (Garrison 1959, Berry 1961).

Mostly the district concept is defined as the regionalization of space or the organization of administrative areas. But also mixtures of both definitions can be found (Tong and Murray 2012).

Examples for created administrative areas include school districts, election districts, post office districts, and the horizontal hierarchical division of countries, among others. Like in the latter example often districts contain smaller partitioning. Figure shows a partition of a region and their subregion 7.

![Partition](/assets/spatialoptimization/partition.png)

Districts are often used in spatial optimization. Many times the result of spatial optimization problems are districts. Therefore the goal of such a problem is to find the best fitting districts in order to subdivide a region in a balanced way (Tong and Murray 2012). Several outcomes of elections have showed that the creation of adequate election districts is anything but simple.

Noted spatial optimization problems, where the concept of district is implemented, include the creation of school districts (Schoepfle and Church 1991, Church and Murray 1993), the redistriction of political areas (Morrill 1973, Openshaw and Rao 1995, Williams 1995) and the grouping of units (Duque et al. 2011).

The spatial concept of pattern describes the distribution of spatial objects or the organization in space. Mostly pattern characterisation is divided in the categories random, dispersed, and clustered (see figure 8). In early works the concept of pattern was used in order to analyse human settlement focused on the theory of central places (King 1962, Tong and Murray 2012).

![pattern](/assets/spatialoptimization/pattern.png)

Quantitative descriptions of patterns are based on point measurements, like nearest neighbor or k-function, and spatial auto correlation, like Moran’s I. Nevertheless there is no universal accepted index in order to measure and describe patterns (Tong and Murray 2012).

Examples for spatial optimization include the facility location. This techniques can be implemented in order to prevent clustered facility locations. Therefore dispersed patterns are preferred for many facilities.

## How to solve a Spatial Optimization Problem

In order to solve a unique problem, first of all the spatial optimization problem must be formulated with the relationship between the spatial concepts and other attributes.
This abstraction of reality and structuring the model is viewed as sophisticated task, that requires skill and creativity (Church and Murray 2009, Tong and Murray 2012).
Nevertheless a detailed explanation of such a model would exceed the framework of the research question of this seminar paper.

In order to solve a spatial optimization problem there exists two strategies. In the first place exact methods. In the second place heuristic methods (Scott 1971, Church and Murray 2009, Tong and Murray 2012).

The exact methods exploit all possible solutions and are therefore exact methods that find the optimal solution. In contrast heuristic methods are capable to find a solution when exact methods can not solve a problem. This maybe for one of the following reasons. On the one hand the problem can not be solved by an exact methods, because there is no optimal solution. On the other hand an exact solution would exceed available computational power or time limitations (Church and Murray 2009, Tong and Murray 2012).

There are numerous exact approaches, like linear programming, enumeration, integer programming, among others, which can be applied to different models. But also more specific-oriented methods, like the Dijkstra’s algorithm, exist (Church 2001, Tong Murray 2012).

Heuristic methods are based on rules of thumb or procedures designed for specific optimization problems. Many heuristic solutions start with one or a few potential solutions. Based on this solution the heuristic method can be updated and restarts the search for potential solution. With each iteration the results get better and the chances increase that the optimal solution can be found. Nevertheless time restrictions limit the number of iterations (Church 2001, Tong and Murray 2012).

## Sources

* Aerts, J., Eisinger, E., Heuvelink, G., and Stewart, T. (2003). Using linear integer programming for multi-site land-use allocation. Geographical Analysis, 35:148.
* Beaumont, J. R. (1982). Mathematical programming in human geography. Mathematical Social Sciences, 2(3):213 – 243.
* Berry, B. J. L. (1961). A method for deriving multifactor uniform regions. Przeglad Geograficzny, 33:263.
* Bianchi, G. and Church, R. L. (1988). A hybrid fleet model for emergency medical service system design. Social Science & Medicine, 26(1):163 – 171.
* Boyce, R. R. and Clark, W. A. V. (1964). The concept of shape in geography. Geographical Review, 54:561.
* Bunge, W. (1962). Theoretical geography. Gleerup, Lund Sweden.
* Christaller, W. (1966). Central Places in Southern Germany. Prentice Hall, Englewood Cliffs.
* Church, R. L. (1990). The regionally constrained p-median problem. Geographical Analysis, 22(1):22–32.
* Church, R. L. (2001). Spatial optimization models. In Baltes, N. J. S. B., editor, International Encyclopedia of the Social & Behavioral Sciences, pages 14811 – 14818. Pergamon, Oxford.
* Church, R. L. and Bell, T. L. (1988). An analysis of ancient egyptian settlement patterns using location–allocation covering models. Annals of the Association of American Geographers, 78(4):701–714.
* Church, R. L. and Murray, A. T. (1993). Modeling school utilization and consolidation. Journal of Urban Planning and Development ASCE, 119:23.
* Church, R. L. and Murray, A. T. (2009). Business site selection, location analysis, and GIS. John Wiley & Sons, Hoboken, N.J.
* Church, R. L., Stoms, D. M., and Davis, F. W. (1996). Reserve selection as a maximal covering location problem. Biological Conservation, 76(2):105 – 112.
* Curtin, K. M. and Church, R. L. (2006). A family of location models for multiple type discrete dispersion. Geographical Analysis, 38:248.
* de Smith, M. J., Goodchild, M. F., and Longley, P. (2007). Geospatial analysis: A comprehensive guide to principles, techniques and software tools. Matador, Leicester, 2nd ed. edition.
* Duque, J. C., Church, R. L., and Middleton, R. S. (2011). The p-regions problem. Geographical Analysis, 43:104.
* Erdemir, E. T., Batta, R., Rogerson, P. A., Blatt, A., and Flanigan, M. (2010). Joint ground and air emergency medical services coverage models: A greedy heuristic solution approach. European Journal of Operational Research, 207(2):736–749.
* Garrison, W. L. (1959). Spatial structure of the economy: Ii. Annals of the Association of American Geographers, 49(4):471–482.
* Goodchild, M. F. and Massam, B. H. (1969). Some least cost models of spatial administrative systems in southern ontario. Geografiska Annaler, 52(B):86–94.
* Haggett, P. (1975). Geography: A modern synthesis. Harper & Row, New York, 2nd edition.
* Hogan, K. and ReVelle, C. (1986). Concepts and applications of backup coverage. Management Science, 32(11):1434–1444.
* Horner, M. and Downs, J. (2007). Testing a flexible geographic information system-based network flow model for routing hurricane disaster relief goods. Transportation Research Record: Journal of the Transportation Research Board, 2022:47–54.
* Hudak, P. F., Loaiciga, H. A., and Schoolmaster, F. A. (1993). Application of geographic information systems to groundwater monitoring network design1. JAWRA Journal of the American Water Resources Association, 29(3):383–390.
* Kim, K., Murray, A. T., and Xiao, N. (2008). A multiobjective evolutionary algorithm for surveillance sensor placement. Environment and Planning B: Planning and Design, 35(5):935–948.
* Kim, H. O’kelly, M. E. (2009). Reliable p-hub location problems in telecommunication networks. Geographical Analysis, 41(3):283–306.
* King, L. J. (1962). A quantitative expression of the pattern of urban settlements in selected areas of the united states. Tijdschrift Voor Economische en Sociale Geografie, 53:1.
* Kuby, M. J. (1987). Programming models for facility dispersion: The p-dispersion and maximum dispersion problems. Geographical Analysis, 19:315.
* Ligmann-Zielinska, A., Church, R. L., and Jankowski, P. (2008). Spatial optimization as a generative technique for sustainable multiobjective land-use allocation. International Journal of Geographical Information Science, 22(6):601–622.
* Longley, P. (2011). Geographic information systems & science. Wiley, Hoboken, NJ, 3rd ed edition.
* Love, R. F., Morris, J. G., and Wesolowsky, G. O. (1988). Facilities location: Models & methods, volume 7 of Publications in operations research series. North-Holland, New York.
* MacKinnon, R. D. Hodgson, M. J. (1970). Optimal transportation networks: a case study of highway systems. Environment and Planning A, 2(3):267–284.
* Malcolm, S. and ReVelle, C. (2005). Representational success: A new paradigm for achieving species protection by reserve site selection. Environmental Modeling & Assesment, 10(4):341–348.
* Matisziw, T. C. and Murray, A. T. (2006). Promoting species persistence through spatial association optimization in nature reserve design. Journal of Geographical Systems, 8:289.
* Miller, H. J. and Wentz, E. A. (2003). Representation and spatial analysis in geographic information systems. Annals of the Association of American Geographers, 93(3):574–594.
* Morrill, R. L. (1973). Ideal and reality in reapportionment. Annals of the Association of American Geographers, 63:463.
* Murray, A. T., Kim, K., Davis, J. W., Machiraju, R., and Parent, R. (2007). Coverage optimization to support security monitoring. Computers, Environment and Urban Systems, 31(2):133 – 147.
* Nystuen, J. D. (1968). Identification of some fundamental spatial concepts. In Berry, B. J. L. M. D. F., editor, Spatial analysis: A reader in statistical geography, page 35–41. Prentice-Hall, Englewood Cliffs.
* O’kelly, M. E. (1987). A quadratic integer program for the location of interacting hub facilities. European Journal of Operational Research, 32(3):393–404.
* Openshaw, S. and Rao, L. (1995). Algorithms for reengineering 1991 census geography. Environment and Planning A, 27:425.
* Oppong, J. R. and Hodgson, M. J. (1994). Spatial accessibility to health care facilities in suhum district, ghana. The Professional Geographer, 46(2):199–209.
* Reidhead, V. A. (1979). Linear programming models in archaeology. Annual Review of Anthropology, 8(1):543–578.
* ReVelle, C. S. and Swain, R. W. (1970). Central facilities location. Geographical Analysis, 2(1):30–42.
* Schoepfle, O. B. and Church, R. L. (1991). A new network representation of a classic school districting problem. Socio-Economic Planning Sciences, 25:189.
* Scott, A. J. (1971). Combinatorial programming, spatial analysis and planning. Methuen young books, London.
* Shirabe, T. (2005). A model of contiguity for spatial unit allocation. Geographical Analysis, 37(1):2–16.
* Sorensen, P. and Church, R. (2010). Integrating expected coverage and local reliability for emergency medical services location problems. Socio-Economic Planning Sciences, 44(1):8 – 18.
* Tobler, W. (1970). A computer movie simulating urban growth in the detroit region. Economic Geography, 46(2):234–240.
* Tong, D. and Murray, A. T. (2012). Spatial optimization in geography. Annals of th Association of American Geographers, 102(6):1290–1309.
* Von Thunen, J. H. (1826). Der isolirte Staat in Beziehung auf Landwirthschaft und Nationalökonomie. Perthes, Hamburg.
* Weber, A. (1908). Reine Theorie des Standorts. Mohr, Tübingen.
* Wentz, E. A. (2000). A shape definition for geographic applications based on edge, elongation and perforation. Geographical Analysis, 32:95.
* Williams, J. C. (1995). Political redistricting: A review. Papers in Regional Science, 74:13.
* Williams, J. C. (2002). A zero-one programming model for contiguous land acquisition. Geographical Analysis, 34(4):330–349.
* Williams, J. C. and ReVelle, C. S. (2004). Using mathematical optimization models to design nature reserves. Frontiers in Ecology and the Environment, 2:98.
* Wu, X. and Murray, A. T. (2008). Spatial contiguity optimization in land acquisition. Journal of Land Use Science, 2(4):243–256.
