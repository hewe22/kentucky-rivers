
# Kentucky Rivers and Streams by Basin Management Area


## Project Contents


- [Data Source](#data-source)
- [Project Background](#project-background)
- [Purpose](#purpose)
- [Mapmaking Process](#mapmaking-process)
- [Map Summary](#map-summary)
- [Final Project](#final-project-link)

***

### Data Source
All data for this project was sourced from the [KyGovMaps Open Data Portal](https://opengisdata.ky.gov/). 
Data for major rivers and waterways in Kentucky - [Link to data source](https://opengisdata.ky.gov/datasets/kygeonet::kentucky-rivers/explore?location=37.281171%2C-85.984703%2C6)
Data for minor streams and tributaries in Kentucky - [Link to data source](https://opengisdata.ky.gov/datasets/25811a405483466092fe81df34a26532_0/explore?location=37.802965%2C-85.817228%2C7)
Data for Kentucky river basin management units - [Link to data source](https://opengisdata.ky.gov/datasets/3260f895682242a695998c41a2872252_0/explore?location=37.853030%2C-85.785630%2C7)

* Initial Data projection: EPSG:4326 - WGS 84
* Final Map projection: EPSG:3089 - NAD 83 Kentucky Single Zone (ftUS)

### Project Background

Water is a major resource to Kentucky, having the second-most amount of running water (rivers, streams, etc) out of all states in the US. These water resources, therefore, must be managed in an effective way to ensure everyone can utilize them. The Kentucky Watershed Management Framework coordinates existing programs and new partnerships to better manage Kentucky's water resources. This framework divides Kentucky waters into seven distint "Basin Team Areas", each with their own Basin Coordinator who allocates resources and acts as a liason to the community. 

### Purpose

This map is intended to serve as a resource for anyone connected to water in Kentucky. It provides a way to connect with your local water sources and to discover more about the Basin Management Areas that help protect our water resources. Specifically, this map provides an in-depth view of all rivers and streams across the state and to which Basin Management Area they belong.

### Mapmaking Process

Example of in process map ![in process image](filepath)

After adding the river, stream, and basin management boundaries layers to the map,
The Kentucky rivers data extends some of the rivers outside of the state's boundary. To remove the unnecessary vectors, I utilized the "clip" feature in geoprocessing tools. By using the rivers layer as the input layer and a polygon of Kentucky's state boundary, the result is a layer that contains only line data within the bounds of the state.
<img width="853" height="691" alt="image" src="https://github.com/user-attachments/assets/4b7c8b4e-39d0-4ee5-a970-fa88215d57d8" />
For the streams data, I utilized "scale dependent visibility" to avoid showing all of the data when zoomed out. At a map scale of 1:250000, all streams data appears.
<img width="1059" height="871" alt="image" src="https://github.com/user-attachments/assets/43c633ff-6b0f-414e-b176-62bb0760554c" />
For the final layer, basin management areas, it was necessary to distinguish the different areas by altering the style. Under "symbology", I used the "categorized" option to give each management area a different color. I also set the opacity to 50% so that the basemap could be seen underneath it.
<img width="1062" height="879" alt="image" src="https://github.com/user-attachments/assets/16219456-694d-46f8-bfc5-6c33c6227f1a" />


### Map summary

What are the key findings to take from your map and the overall mapmaking process?

## Final Project Link

Here you are linking from the README.md to the index.html.

Please view the [final map online](www.github...)
