# My Toolbox for Visualization

## Bokeh (Updating)
### Data source: 
A json object form: http://ncov.nosensor.com:8080/api/ and find it here:[api.json](https://github.com/ZhijunLiu96/Visualization/blob/master/data/api.json)

Then [extract](https://github.com/ZhijunLiu96/Visualization/blob/master/data/json_to_csv.ipynb) province data and save to [data.csv](https://github.com/ZhijunLiu96/Visualization/blob/master/data/data.csv)

### China Map
Visualized number of confirmed cases until 2020-02-12, and used two python objects to create the map template.([GitHub source](https://github.com/sdq/bokeh-china-map)). Clicking each button on the right can check the detailed information for each province, including the number of close contacts, confirmed cases, critical cases, cured cases, and dead cases.
```python
class China():
class ChinaMap():
```
```python
# set a time
time = '2020-02-12'
```
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/bokeh/figure/chinaMap.png"> 

### Line Charts
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/bokeh/figure/hubeiLine.png">

### ipynb file [Bokeh.ipynb](https://github.com/ZhijunLiu96/Visualization/blob/master/bokeh/Bokeh.ipynb)

### Output file [chinamap.html](https://github.com/ZhijunLiu96/Visualization/blob/master/bokeh/chinamap.html)


## Matplotlib
### Bar charts
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/barChart.png">

### Survey bar charts
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/surveyChart.png">

### ipynb file [matplotlib_example.ipynb](https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/matplotlib_example.ipynb)

### How data visualization helps with decision making? [example_report.pdf](https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/example_report.pdf)

