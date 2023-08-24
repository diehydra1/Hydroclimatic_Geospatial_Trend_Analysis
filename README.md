# Hydrology_Hydroclimatic_Geospatial_Trend_Analysis
The Spree, a second-order tributary of the Elbe with a UNESCO Biosphere Reserve named Spreewald, is already water-stressed due to anthropogenic activities 
and natural conditions. Recent studies show that increasing evapotranspiration and land use patterns have exacerbated groundwater level depletion. 
A continuous hydrological model, the Soil and Water Assessment Tool (SWAT) was used to quantify existing groundwater recharge in the Lower Spree region. 
The model was simulated for 50 years and calibrated using SWAT-CUP. The annual water balance was calculated, revealing the region is water stressed, 
with a mean annual groundwater recharge of 76.54 mm with a declining trend. The model also provided insights into the spatiotemporal distribution of groundwater recharge,
with most of the distribution observed in forested and irrigated regions. The temporal analysis showed an increasing trend in winter, while in summer and spring, 
it showed a downward trend.

## Table of content

- [Code description](#Code-description)
- [Getting Started](#Getting-Started)
- [Prerequisites](#Prerequisites)
- [Usage](#Usage)

## Code description
### Data Visualisation for Streamflow and Evapotranspiration (ET) Using Bokeh
The project uses the Bokeh library to visualize streamflow data, generating an interactive display after reading real and simulated data from CSV files. Key features include a changeable datetime x-axis, an interactive tooltip, and a dual y-axis representation for discharge and precipitation. The main script imports Pandas and Bokeh modules for data manipulation. The Bokeh figure includes discharge line graphs, precipitation bar graphs, customizable labels, and hover tools for interactive data visualization.

#### Hydrological Evaluation, Groundwater Recharge, and Hydrocliamtic Analysis for SWAT Subbasins
This Python script is designed for analyzing hydrological characteristics in different hydrologic response units (HRUs) and subbasins, such as groundwater recharge, evapotranspiration (ET), and precipitation. The Lower Spree catchment's recharge trend is the main focus of the script, which employs data manipulation and visualization to provide insightful information on Spatial distribution. Geographical data and the results of hydrological models are the main data sources.
Key Features but not limited to
1. Calculation of groundwater recharge, ET, and precipitation for each SWAT HRU and subbasin for the Lower Spree catchment
2. Area-weighted computation of these hydrological features to provide a comprehensive analysis and spatial distribution
3. Integration with GeoPandas for spatial data manipulation
4. Utilization of Matplotlib for data visualization
5. Visualization of Evapotranspiration (ET) rates across subbasins
   
   
## Getting Started

### Prerequisites
To run this code, the following packages need to be installed in the Anaconda environment:

1. Open anaconda prompt.

2. Activate the environment you want to work with.

   ```
   conda activate [enviornment name] 
   ```

3. Install the following by using given commands.

   ```
   pip install pandas numpy bokeh matplotlib geopandas shapely simple_colors

   ```

### Usage
Data Preparation: It is requested that an accessible directory be chosen for the observed and simulated CSV files to be placed in both for Discharge and ET. A “Date” column in the CSV files is required. The script should have the path to the intended CSV files updated.

```
jupyter nbconvert --execute Discharge_Bokeh_Plotting.ipynb
```
```
jupyter nbconvert --execute ET_Bokeh_Plotting.ipynb
```
The script will generate an HTML file containing the interactive Bokeh plot, which can also be visualized with a web browser.
The following picture shows how the developed script provides the output streamflow and ET time series for the same gauging point:

![](/Bokeh%20Plotting_Discharge_ET/Discharge/Outputs%20for%20Discharge/99_Beeskow.png)
![](/Bokeh%20Plotting_Discharge_ET/ET/Outputs%20for%20ET/99_Beeskow.png)

```
jupyter nbconvert --execute groúndwater_recharge_cal.ipynb
```
The computed groundwater recharge, ET, and precipitation data for the HRUs and SWAT subbasins are available after successful execution with temporal resolution 
on a daily basis. Pandas DataFrames are used to store the outcomes. One may adapt the code to plot these characteristics on maps in order to visualize the data.
The 600 dpi resolution visualizations will be stored in the out_fig subfolder. The catchment's climate at the time the data were taken will be reflected in the filenames.
The following picture shows how the developed script provides the output streamflow and ET time series for the same gauging point:

![](/Ground%20Water%20Recharge%20Calculation/fig_gw/gw_et_geo.png)
![](/Ground%20Water%20Recharge%20Calculation/fig_gw/gw_precip_geo.png)
![](/Ground%20Water%20Recharge%20Calculation/fig_gw/gw_daily_geo.png)

## Acknowledgements
The script development and automated analysis are part of the research work for the MSc. Thesis, BMBF project SpreeWasser: N, aimed at developing innovative Integrated Water Resources Management (IWRM) tools and strategies
under the supervision of Prof. Dr.-Habil. Irina Engelhardt from the Technical University of Berlin and in association with the co-supervision of Prof. Dr.-Ing. Rainer Helmig from LH2, Universiät Stuttgart.
