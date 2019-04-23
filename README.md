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

Cars.png!
![Altair Visualization](https://github.com/dvgnaveenkumarreddy/datavisualization/blob/master/Cars.png)

