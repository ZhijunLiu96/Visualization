# My Toolbox for Visualization

# Bokeh (Updating)
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

### Want to do: plot indicator to show how to allocate resouces among different provinces.

### ipynb file [Bokeh.ipynb](https://github.com/ZhijunLiu96/Visualization/blob/master/bokeh/Bokeh.ipynb)

### Output file [chinamap.html](https://github.com/ZhijunLiu96/Visualization/blob/master/bokeh/chinamap.html)


# Matplotlib


## ipynb file [matplotlib_example.ipynb](https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/matplotlib_example.ipynb)
### Bar charts
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/barChart.png">

### Survey bar charts
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/surveyChart.png">

### How data visualization helps with decision making? [example_report.pdf](https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/example_report.pdf)

## ipynb file [StackedBarChat_Subplot_Subplots.ipynb](https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/StackedBarChat_Subplot_Subplots.ipynb)
Data:[score.csv](https://github.com/ZhijunLiu96/Visualization/blob/master/data/score.csv)

### subplot
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/subplot.png">

### Subplot with Stacked bar chart 

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

```python
plt.figure(figsize=(20,10))

plt.subplot(121)
plt.barh(index0, x0, color="lightsteelblue")
plt.barh(index0, x1, left=x0, color="royalblue")
plt.barh(index0, x2, left=x01, color="navy")
plt.legend(['completeness = 0', 'completeness = 1', 'completeness = 2'])
plt.xlabel('Number of corps (2964 in total)', fontsize=16)  
plt.ylabel('Indicators', fontsize=16)
plt.grid(True)
plt.title('Distribution of completeness in 2018', fontsize=16)

plt.show()
```
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/stacked_bar.png">

### Subplot vs Subplots

```python
x_labels = ['0', '1', '2']
width = 0.2 # width of bar
x = np.arange(3)
plt.figure(figsize=(32,4))

index_=1
for i in range(8):
    order = 181+i
    plt.subplot(order)
    d2017 = list(data2017.iloc[i,:])
    d2018 = list(data2018.iloc[i,:])
    plt.bar(x + 2*width, d2018, width, color='#000080', label='2018')
    plt.bar(x + width, d2017, width, color='#6593F5', label='2017')
    if index_ == 1:
        plt.ylabel('Number of Corps')
    plt.xlabel('Completeness')
    plt.xticks(x + width + width/2,x_labels)
    plt.title('Indicator: {}'.format(ind[i]))
    plt.legend()
    plt.grid(True)
    index_ += 1

plt.show()
```
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/subplot2.png">

**While subplots function can easily plot more than 10 plots**
<img src="https://github.com/ZhijunLiu96/Visualization/blob/master/matplotlib/figure/subplots.png">
