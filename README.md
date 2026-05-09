
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

Data for Kentucky Waterbodies - [Link to data source](https://opengisdata.ky.gov/datasets/15aa661687474a6d997022ee24e98128_0/explore?location=36.982832%2C-86.451117%2C10)

* Initial Data projection: EPSG:4326 - WGS 84
* Final Map projection: EPSG:3089 - NAD 83 Kentucky Single Zone (ftUS)

### Project Background

Water is a major resource for Kentucky, having the second-most amount of running water (rivers, streams, etc) out of all states in the US. These water resources, therefore, must be managed in an effective way to ensure everyone can utilize them. The Kentucky Watershed Management Framework coordinates existing programs and new partnerships to better manage Kentucky's water resources. This framework divides Kentucky waters into seven distint "Basin Team Areas", each with their own Basin Coordinator who allocates resources and acts as a liason to the community. For more information on Basin Management Areas, visit the Kentucky Energy and Environment Cabinet website [here](https://eec.ky.gov/Environmental-Protection/Water/Outreach/BasinCoordination/Pages/default.aspx).  

### Purpose

This map is intended to serve as a resource for anyone connected to water in Kentucky. It provides a way to connect with your local water sources and to discover more about the Basin Management Areas that help protect our water resources. Specifically, this map provides an in-depth view of all rivers and streams across the state and to which Basin Management Area they belong.

### Mapmaking Process

After adding the river, stream, and basin management boundaries layers to the map,
The Kentucky rivers data extends some of the rivers outside of the state's boundary. To remove the unnecessary vectors, I utilized the "clip" feature in geoprocessing tools. By using the rivers layer as the input layer and a polygon of Kentucky's state boundary, the result is a layer that contains only line data within the bounds of the state.
![Parameters of "clip" geoprocessing tool](graphics\vector-overlay-clip.png)
<img width="853" height="691" alt="image" src="https://github.com/user-attachments/assets/4b7c8b4e-39d0-4ee5-a970-fa88215d57d8" />

For the streams data, I utilized "scale dependent visibility" to avoid showing all of the data when zoomed out. At a map scale of 1:250000, all streams data appears.
![Settings for scale dependent visibility](graphics\scale-dependent-visibility.png)
<img width="1059" height="871" alt="image" src="https://github.com/user-attachments/assets/43c633ff-6b0f-414e-b176-62bb0760554c" />

For the final layer, basin management areas, it was necessary to distinguish the different areas by altering the style. Under "symbology", I used the "categorized" option to give each management area a different color. I also set the opacity to 50% so that the basemap could be seen underneath it.
![Settings for categorized symbology](graphics\categorized-symbology.png)
<img width="1062" height="879" alt="image" src="https://github.com/user-attachments/assets/16219456-694d-46f8-bfc5-6c33c6227f1a" />

The labels for major kentucky waterways and waterbodies have scale dependent visibility, with labels appearing at a minimum zoom of 1:250,000.
![Settings for scale dependent visibility of labels](graphics\labels-scale-dependent-visibility.png)
<img width="1060" height="877" alt="image" src="https://github.com/user-attachments/assets/6d5310ba-eabd-46f0-b5f7-0242257affef" />

To avoid a map full of minor lake labels, set the "suppress labeling of features smaller than" option to 3.0mm.
![Map view of lakes labels without adjust label visibility](graphics\non-filtered-lake-labels.png)
<img width="1483" height="767" alt="image" src="https://github.com/user-attachments/assets/de701c59-df67-4fff-9b11-c415871970c6" />

### Map summary

The key findings from my map are that water connects Kentucky. No matter where you go in the state, you will find water. It is an invaluable resource that we often take for granted here in Kentucky. As we have witnessed recent droughts across the country, however, it brings into focus just how important our waterways are. Knowing where your water comes from and how it is protected is vital to its long term safety. 
As for my mapmaking journey, I learned about using state versus national data. In many cases, statewide data is not standardized in the same way as national data, which can make it much harder to utilize. For instance, the Kentucky Rivers data only contained "larger" waterways, without providing exact specifications for why certain data were included over others. Even after looking through the metadata for the layer, I couldn't find whether the selections were based on stream order, navigable waterways, or something else. Moving on to the Assessed Streams data, it contained many of the smaller streams and creeks across the state, while also incorporating some of the larger waterways. Again, there was no way for me to isolate larger or smaller streams based on stream order, only by total length which is not a useful metric for the discernment of waterways. This lack of manipulability in the layer prevented me from utilizing it to the fullest.

## Final Project Link

Please view the [final map online](https://hewe22.github.io/kentucky-rivers)
