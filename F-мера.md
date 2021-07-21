# F-мера
$F_{\beta}$

$$F_{\beta} = \frac{2 * precision * recall}{precision + recall}$$

[[Среднее гармоническое]] precision и recall

F-мера стремится к 1 при обновременно больших precision и recall, и к нулю, если хотя бы один из них близок к нулю.

[[precision]], [[recall]] и [[F-мера]] есть в sklearn в metrics.classification_report

```python
from sklearn.metrics import precision_recall_curve, classification_report

report = classification_report(y_test, lr.predict(X_test), target_names=['Non-churned', 'Churned'])
print(report)
```