NOTE :  This Project Under Devolpment to know More on [github](https://github.com/KrezyKiller/dchartjs/)  

# dchartjs

dchartjs is python package. it is used to draw charts in frontend Using Python
## Installation

Use the package manager [pip](https://pypi.org/project/dchartjs/) to install dchartjs. 

```bash
pip install dchartjs
```

## Basic Usage In Django
in Django views.py
```python
from dchartjs.basic_chart import Bchart

def DjangoChart(request):
    Chart = Bchart()
    Chart.chart_data(xdata=[0,2,5,10],ydata=[1,5,5,25])
    data = Chart.project_djangoview()
    return render(request, 'chart.html', data)
```
in chart.html
```html
<body>
{{ chart_as }}
</body>
```
## Basic Usage In No Framework
if your not using any Framework then you can also plot directly into web. 
in chart.py
```python
from dchartjs.basic_chart import Bchart

Chart = Bchart()
Chart.chart_data(xdata=[0,2,5,10],ydata=[1,5,5,25])
Chart.project_web() #it create temp.html file then open chart in browser 
```
now run
```python
python chart.py
```
## Basic Style dchartjs
```python
from dchartjs.basic_chart import Bchart

def DjangoChart(request):
    Chart = Bchart()
    Chart.chart_style_conf(width=100,height=100) 
    Chart.chart_data(xdata=[0,2,5,10],ydata=[1,5,5,25])
    data = Chart.project_djangoview()
    return render(request, 'chart.html', data)
```
