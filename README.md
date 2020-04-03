# DVI-Toolboxes
ArcGIS ModelBuilder Files Used to Create Daily KDE Hotspot Forecasts and a Measure of Dynamic Variability

There are 7 model builder files in this toolbox file, representing the 7 steps taken to convert crime incident 
location data points that are represented as discrete locations into an exportable Excel file that can be used 
to measure the daily changes in crime hotspot patterns. 

Each of the 7 files is labled with the "step" number in the process, along with a descriptions of that step. The file/step
names are as follows:

(Step 1) Create 365 SHP Files from Full File
(Step 2) Create 365 KDE files from SHPs
(Step 3) Reclassify 365 Rasters to Significant Hotspots
(Step 4) Create 365 Raster files for D R and E
(Step 5) Create 365 Raster Tables for D R and E
(Step 6) Create 365 Excel Tables for D R and E
(Step 7) Appends 365 DD R and E files.

When all 7 models are run, an Excle file containing the nubmer of grid cells at Time n + 1 predictions will be created.
For each of the 365 KDE maps produced, hotspots at Time n + 1 predictions will be classified into one of three types: 

(1) a repeating hotspot (R) or a hotspot cell that appeared in both the Time n 
and Time n + 1 prediction maps; 

(2) an emerging hotspot (E) or a hotspot cell that was present in the Time n + 1 prediction 
map, but not in the Time n map; or 

(3) a disappearing hotspot (D) or a hotspot cell that was present in the Time n prediction 
map, but not in the Time n + 1 map. 

To produce the Dynamic Variability Index (DVI) score, the total number of newly emerging hotspot cells in a study 
area (E) for a given interval should be divided by the total number of hotspot cells in the same area that was 
either newly emerging or repeating (i.e., E + R).
