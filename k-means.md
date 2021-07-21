# Метод k-средних
## метод главных точек
Наиболее популярный метод кластеризации.

Стремится минимизировать суммарное среднее квадратичное отклонение объектов в кластерах от центров кластеров.

Минусы: 
* кол-во кластеров нужно знать заранее (подбирать).
* Не всегда достигается глобальный миниммум, часто это локальный.
* оптимальный выбор центров кластеров неизвестен. 

Существует так же [[k-means++]] улучшенная версия алгоритма
https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html

```python
>>> from sklearn.cluster import KMeans
>>> import numpy as np
>>> X = np.array([[1, 2], [1, 4], [1, 0],
...               [10, 2], [10, 4], [10, 0]])
>>> kmeans = KMeans(n_clusters=2, random_state=0).fit(X)
>>> kmeans.labels_
array([1, 1, 1, 0, 0, 0], dtype=int32)
>>> kmeans.predict([[0, 0], [12, 3]])
array([1, 0], dtype=int32)
>>> kmeans.cluster_centers_
array([[10.,  2.],
 [ 1.,  2.]])
```
