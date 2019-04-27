Here is an example using Altair to quickly visualize and display a dataset with the native Vega-Lite renderer in the JupyterLab:

```python
import altair as alt
from vega_datasets import data

# for the notebook only (not for JupyterLab) run this command once per session
#alt.renderers.enable('notebook')

iris = data.iris()

alt.Chart(iris).mark_point().encode(
    x='petalLength',
    y='petalWidth',
    color='species'
)
```
Here is image

![Altair Visualization](https://github.com/dvgnaveenkumarreddy/datavisualization/blob/master/Iris.png)


```python
# load an example dataset
from vega_datasets import data
cars = data.cars()

# plot the dataset, referencing dataframe column names
import altair as alt
alt.Chart(cars).mark_point().encode(
  x='Horsepower',
  y='Miles_per_Gallon',
  color='Origin'
).interactive()
```
Here is image

![Altair Visualization](https://github.com/dvgnaveenkumarreddy/datavisualization/blob/master/Cars.png)

```python
# load an example dataset
from vega_datasets import data
cars = data.cars()

# plot the dataset, referencing dataframe column names
import altair as alt
alt.Chart(cars).mark_bar().encode(
  x='mean(Miles_per_Gallon)',
  y='Origin',
  color='Origin'
)
```
Here is image

![Altair Visualization](https://github.com/dvgnaveenkumarreddy/datavisualization/blob/master/Cars1.png)
