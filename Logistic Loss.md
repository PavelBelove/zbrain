В основе [[максимизации правдоподобия]], но поскольку там произведение вероятностей, заводим $\hat{y_i}$ под знак логарифма - сумму оптимизировать проще.

$$LogLoss=-\frac{1}{l}\sum_{i=1}^l[y_i⋅log_e(\hat{y_i})+(1−y_i)⋅log_e(1−\hat{y_i})]$$

Где $\hat{y_i}$ - ответ алгоритма на i объекте а $y_i$ - истинное значение. l - размер выборки.

Метрика редко используется в бизнесе, часто на [[Kaggle]]

По сути, максимизирует [[accuracy]], очень сильно штрафует алгоритм, если классификатор был уверен в неверном ответе.

```python
def logloss_crutch(y_true, y_pred, eps=1e-15):

    return - (y_true * np.log(y_pred) + (1 - y_true) * np.log(1 - y_pred))

print('Logloss при неуверенной классификации %f' % logloss_crutch(1, 0.5))
>> Logloss при неуверенной классификации 0.693147

print('Logloss при уверенной классификации и верном ответе %f' % logloss_crutch(1, 0.9))
>> Logloss при уверенной классификации и верном ответе 0.105361

print('Logloss при уверенной классификации и НЕверном ответе %f' % logloss_crutch(1, 0.1))
>> Logloss при уверенной классификации и НЕверном ответе 2.302585
```