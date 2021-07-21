# Заголовок (#)
## подзаголовок (## - ####)
*курсив* 
**жирный** (две звездочки) ^614752
_курсив_
__жирный__
~~зачеркнутый~~
==текстовыделитель== (только в обсидиан)

```
Типографический текст
    Или код
        С форматированием
        Кавычка с клавиши Ё
```

```javascript
var s = "Подсветка JavaScript";
alert(s);
```

```python
s = "Подсветка Python"
print s
```



[[заметки]] - сылка
[[markdown#подзаголовок -]] Cсылка к конкретному разделу (работает только в обсидиан)
[[markdown#^614752]] сылка на конкретную строку
![[obsidian]] Встраивание текста из ссылки в карточку (! перед ссылкой)

[Видео по маркдаун](https://www.youtube.com/watch?v=IuqWQtOZd8Q) (пример внешней ссылки)

#markdown - без пробела ([[тег]])

---
[[Метаданные]]
___
[[Метаданные]]

Картинка
![картинка](https://wiki.merionet.ru/images/networkAcademy.png)

- список 1
- список 2
1. номерованный
    1. Вложенный
> цитата [^1]
[^1]:сноска по цитате

колонка1|колонка2
:---|---:
Двоеточие| выравнивание по краю

- [ ] чеклист
- [X] выполнено 

Внутренняя ссылка: 
куда ссылаемся 
```
<a id='hw'></a>
```

Откуда ссылаемся:
```
[Ссылка на домашнее задание](#hw)
```