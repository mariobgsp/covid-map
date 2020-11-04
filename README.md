# COVID19-MAP
A COVID-19 MAP based on Total Death and Total Active Cases on every country in the world by coursera project networks

here is the full line of code [covid-map1.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb), the dashboard would look like this,
* my-covidmap: https://mariobgsp.github.io/covid-map/

## Code Breakdown
### importing modules
Python modules that i used for this project including,
* **json** to convert data from API
* **folium** to generate map in this project
* **request** & **http.client** to get Access of the Data via API
* **pandas** to normalize the data

![modules](/images/modules.jpg)

### Accessing and Normalize the Data
After importing modules, we're trying to acces Data via API the sites that i'm using for API is from covid19api.com using these line of code, to access data, to convert Data to JSON, and Normalize data using python pandas

![load_database](/images/first_step.jpg)

imported dataframe would be like this,

![dataframe_API](/images/dataframe_API.png)

you can drop unnecessary columns to make data processing easier, but if you're not just don't (optional)

![dropping_columns](/images/dropping_columns.png)

### Visualize Data
#### Generating Base Map
After that we're trying to generate base map using folium modules, using Stamen Terrain tiles, and trying to obtain geodata from [here](https://raw.githubusercontent.com/python-visualization/folium/master/examples/data)

![generate_basemap](/images/generate_basemap.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

#### Generating Choropleth Map
Now we're trying to generate choropleth map too, the purpose of choropleth map is to provide an easy way to visualize how measurement (height) varies across a geographic area or show the level of variability region [1](https://en.wikipedia.org/wiki/Choropleth_map#:~:text=Choropleth%20maps%20provide%20an%20easy,of%20variability%20within%20a%20region.)

![generate_choropleth](/images/generate_choropleth.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

and then we're trying to visualize circular markers which show the total confirmed and total recovered in every country, and merge it with choropleth map.

Datasets of longitude and latitude of every country you can get in [here](https://raw.githubusercontent.com/VinitaSilaparasetty/covid-map/master/country-coordinates-world.csv)

![generate_cm](/images/generate_cm.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

Choropleth map with circular marker will look like this, the circular markers describe Total Confirmed Case & Total Recovered in every country.
![choropleth_with_cm](/images/choropleth_with_cm.jpg)

#### Generating Heat Map
Generating Base Map with Black and White colours to make heat map visualize better, and adding a heat map layer, the line of code would be like this, 

![baseforheat](/images/baseforheat.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

![generate_basemap_for_heatmap](/images/generating_basemap_for_heatmap.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

Now we're adding Circular Marker to Heat Map, line of code would be like this,

![heat_with_circlemarks](/images/heat_with_circlemarks.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

and the Final Heat Map which only showing total death, would be like this,

![heatmap_totaldeath.jpg](/images/heatmap_totaldeath.jpg)
*full line of code at [covid-map.ipynb](https://github.com/mariobgsp/covid-map/blob/main/covidmap1.ipynb)*

```
End Line of Code

mariobgsp 
newbie to programming worlds
November 2020
```
