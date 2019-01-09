# Data_Pandas
Only code and tips about Pandas


[Introduction to Pandas](http://nbviewer.jupyter.org/urls/gist.github.com/fonnesbeck/5850375/raw/c18cfcd9580d382cb6d14e4708aab33a0916ff3e/1.+Introduction+to+Pandas.ipynb/).

## Observaciones
```python
data['value'] = data.value
type(data.value) = type(data[['value']])
```
### Borrar columnas 
```python
del data['month']
```

![static 1](https://user-images.githubusercontent.com/17385297/50919833-a919e180-1422-11e9-90da-c9d113044524.PNG)


```python
slg = lambda x: (x['h']-x['X2b']-x['X3b']-x['hr'] + 2*x['X2b'] + 3*x['X3b'] + 4*x['hr'])/(x['ab']+1e-6)
baseball.apply(slg, axis=1).apply(lambda x: '%.3f' % x)
```


![static 2](https://user-images.githubusercontent.com/17385297/50920678-c3ed5580-1424-11e9-82bc-5c0278e24ef6.PNG)

```python
baseball.hr.order(ascending=False)
```

```python
baseball.sum()
baseball.mean()

```


[Data Wrangling with Pandas](http://nbviewer.jupyter.org/urls/gist.github.com/fonnesbeck/5850413/raw/3a9406c73365480bc58d5e75bc80f7962243ba17/2.+Data+Wrangling+with+Pandas.ipynb/).



```python
vessels.type.value_counts()

```

The stack method rotates the data frame so that columns are represented in rows:
```python
stacked = cdystonia.stack()
stacked.unstack().head()
```



Value replacement
```python
treatment_map = {'Placebo': 0, '5000U': 1, '10000U': 2}


cdystonia['treatment'] = cdystonia.treat.map(treatment_map)
cdystonia.treatment
```



[Plotting and Visualization](http://nbviewer.jupyter.org/urls/gist.github.com/fonnesbeck/5850463/raw/a29d9ffb863bfab09ff6c1fc853e1d5bf69fe3e4/3.+Plotting+and+Visualization.ipynb/).

[Statistical Data Modeling](http://nbviewer.jupyter.org/urls/gist.github.com/fonnesbeck/5850483/raw/5e049b2fdd1c83ae386aa3205d3fc50a1a05e5b0/4.+Statistical+Data+Modeling.ipynb/).


https://www.kdnuggets.com/2015/11/seven-steps-machine-learning-python.html/2



http://nbviewer.jupyter.org/github/donnemartin/data-science-ipython-notebooks/blob/master/scikit-learn/scikit-learn-intro.ipynb

http://nbviewer.jupyter.org/github/rhiever/Data-Analysis-and-Machine-Learning-Projects/blob/master/example-data-science-notebook/Example%20Machine%20Learning%20Notebook.ipynb
