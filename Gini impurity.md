Gini impurity (Джини загрязненность)

Как и [[Gini]]  coefficient измеряет "равномерность" но эту метрику используют [[деревья решений]].

$$Gini = 1 - \sum_{i=1}^np_i^2$$

$p_i^2$ - частоты представления разных классов в листе дерева.

Если разделение удачно, какая-то частота p будет стремиться к 1, соответственно сумма тоже будет близка к 1, а 1-сумма - к 0. При максимально равномерном же разделении Gini максимально.