![Data vis](https://abovethelaw.com/wp-content/uploads/2015/06/data-visualization.jpg)
# :sparkles:	"Less code, Efficient & time saver" do more interactive Data Visualization with Plotly Express (python lib).

Wow! finally I found this `plotly_express` a new interactive python lib from plotly, so far this is one of the best Data visualization lib I have ever used in python. I liked the way it makes Dark template, interactive labels.

```python
import plotly_express as px
import matplotlib.pyplot as plt
%matplotlib inline
gapminder = px.data.gapminder()
#gapminder2007 = gapminder.query("year == 2007")

pd = px.scatter(gapminder, x="gdpPercap", y="lifeExp",template='plotly_dark',color='continent',labels = dict(lifeExp='Life Exceptancy',gdpPercap = 'GDP/Capita'))

```
![](plotly_express.png)
```python 
gapminder.head()
```
![](table.view.png)
```python

gap2007 = gapminder.query('year == 2007')
px.scatter(gap2007, x="gdpPercap", y="lifeExp",template='plotly_dark',color='continent',hover_name='country',size='pop',size_max=60,labels = dict(lifeExp='Life Exceptancy',gdpPercap = 'GDP/Capita'))
```
>In a single line by just writing `hover_name`,`size` and `labels` we can interactively show the visualization on python.

![](Animation.gif)
