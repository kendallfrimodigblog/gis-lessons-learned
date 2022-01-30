# GIS modeling in 2022, where to begin

![](https://images.unsplash.com/photo-1460186136353-977e9d6085a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80)

January 28th, 2022
<br>
Kendall Frimodig

<br><br>

### A brief history of the past 6 years

<br>

<p style="line-height:2">
Around 6 years ago I began my journey in data analytics, as I enrolled in a two year
masters program in Epidemiology. In retrospect this was rather poor timing; as I began my
study in 2016 the field at large began to take off in a revolutionary way, and I was quite
oblivious to these developments as I found my field of practice either insulated or resistant to such an overhaul.
</p>

<p style="line-height:2">
Today I will focus primarily on providing cliff notes for someone undertaking their first geostatistical project today - but I must first defend my caveman like methods employed just 4 years ago, when I completed my first geospatial predictive model
Here are a few illustrations of the developments taking place from 2016-2018.
</p>


<br>
- development of data science libraries take off

<br>

![](https://cdn-images-1.medium.com/max/1440/1*jvIeor-77F1CRx0fJYCJHA.png)

<br>

- the number of declared data science professionals double in my first year, and triple in my second year of school. [source](https://elu.nl/where-do-data-science-experts-exists)

<br>

![](https://cdn-images-1.medium.com/max/1440/1*Kqe4GA9R69l6F1fGwt5q8g.png)

<br>

- technical blog posting becomes saturated, to the point where there's almost 10+ personal tutorials for a **very specific**
API, python library, or GIS method I'm trying to understand. (not upset)
[source](https://medium.com/feedium/how-many-stories-are-published-on-medium-each-month-fe4abb5c2ac0)

<br>

![](https://miro.medium.com/max/700/1*Ghj4Pi745j7CheQRm9MqsQ.png)

<br>

- very high resolution satellite imagery becomes the norm (if you have the coin,
[source](https://medium.com/radiant-earth-insights/commercial-entrants-are-driving-innovation-in-earth-observation-and-that-is-all-good-f755e2433ae6))

<br>

![](https://miro.medium.com/max/2000/1*Vj_jopLB3ggQVURqdL21Rw.png)

<br>

- satellites are deployed in droves  [source](https://allthingsnuclear.org/syoung/number-of-satellites-skyrockets) (mind the footnote!!)

<br>

![](https://allthingsnuclear.org/wp-content/uploads/2021/07/growth-of-sattelites-bar-graph.jpg)

<br>

<p style="line-height:2">
With the pace we're seeing here, it will likely take some time for such changes to be reflected in textbooks. If you're working on a more advanced spatial regression problem, you might still want to crack open the textbook as there's many methods and associated parameters worth tuning. If you're looking to calculate a vegetative index, or classify land use characteristics, I have great news. </p>



### GIS in the cloud

<br>
<p style="line-height:2">
In short, sophisticated data analysis including geospatial variants are simply more feasible in 2022. The bulk of my time spent on my first project involved the acquisition of orthoimagery, stitching of raster datasets, sampling and projecting to grids, and running local cluster analysis on such data. CPU time was certainly a limiting factor, with some functions running for up to 24 hours in ArcMap. As an example, if you wanted the best public imagery for a analysis of texas, this would amount to roughly 4 TB of data.</p>
<br>

<p style="line-height:2">
All of that pre-processing, and even modeling can now be done in the cloud! Sentinel-2
is currently the highest resolution, public satellite imagery source available (if time of image not as important, NAIP imagery is best as its taken from an airplane and 1m or lower resolution). Google earth engine is a repository for public and proprietary imagery, and an interactive application for suitable for most analysis.</p>

<br>
<p style="line-height:2">
Both have API's which can be called in a local python instance, and with a few days of study both can be queried to obtain model-ready raster data, without ever having to download raw imagery. For earth engine, you can actually apply simple calculations such as a NDVI or land type classification, with the javascript console or from python if you intend the results to be stored to be stored to google cloud storage.</p>

<br>
<p style="line-height:2">
Start your new project here, with the technical walk-throughs provided, and you will have far more time to invest in the creative and intellectually stimulating side of this work: solving the problem, visualizing the data, posing future questions for investigation.</p>

<br>

### Final Thoughts

<br>
<p style="line-height:2">
The modern GIS workflow is highlighted by outsourcing storage and computational resources, applying neural networks for object classification, and leveraging imagery with higher spatial and temporal (detail, frequency of snapshots) resolution to tackle problems not imagined previously. Particularly, the reduced cost and software now available for DIY style drone based data collection has shown great promise - resolution of < 10 cm often. 
</p>

<br>
<p style="line-height:2">
With the marked increase in data-science libraries, enhancement of data collecting instruments,
and ability to leverage cloud computing resources, one can breeze past the grueling pre-processing steps which were in the very recent past a standard.
</p>
<br>
<br>

**Here are a few helpful tutorials for understanding earth observation (EO) data, sentinel hub, and google earth engine.**

<br>

Introductions

- Radiant Earth infographics, invaluable cheatsheats.. [link](https://www.radiant.earth/infographics/)

- Guided jupyter tutorial for working with EO in python and scripting in earth engine.. [link](https://www.youtube.com/watch?v=j15MryznWn4)

<br>


Earth engine


- Earth Engine 101.. [link](https://www.youtube.com/watch?v=oAElakLgCdA)

- Earth Engine Tutorials and Documentation.. [link](https://developers.google.com/earth-engine/tutorials/videos?hl=hr)
- Workflow for using full google cloud stack for Earth Engine (with this, you could conduct a project from your phone!)..[link](https://www.youtube.com/watch?v=CKYPhCwyoy4)

- Land type classification, from python using supervised classification.. [link](https://www.youtube.com/watch?v=Nkd9zHrou9U)

<br>

Sentinel Hub

- Python api workflow.. [link](https://medium.com/sentinel-hub/tk-why-its-time-to-stop-processing-satellite-imagery-on-your-laptop-a09dbf8c72c0)

- Scripting documentation.. [link](https://www.sentinel-hub.com/develop/custom-scripts/)

- Python library.. [link](https://sentinelhub-py.readthedocs.io/en/latest/index.html)
