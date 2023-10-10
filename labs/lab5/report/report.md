---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Дисциплина: Научное программирование"
author: "Полиенко Анастасия Николаевна, НПМмд-02-23"

## Generic options
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
#lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить матричные преобразования для графиков.

# Задание

1. Изучить подгонку полиномиальной кривой с помощью МНК
1. Изучить построение графов
1. Изучить повороты изображения
1. Изучить отображения изображения
1. Изучить дилатацию изображения

# Выполнение лабораторной работы

## Подгонка полиномиальной прямой

1. Создадим матрицу данных и отдельные вектора *x* и *y* (рис. @fig:001), которые в графическом представлении имеют вид (рис. @fig:002).

![Исходные данные. Матрица и векторы](image/1.png){#fig:001 width=60%}

![Исходные данные. График](image/2.png){#fig:002 width=70%}

2. Мы хотим подогнать наши данные под кривую $y = a_1 x^2 + a_2 x + a_3$. Для этого создадим матрицу *A* (рис. @fig:003).

![Матрица А](image/3.png){#fig:003 width=70%}

3. Найдём коэффициенты (рис. @fig:004).

![Коэффициенты](image/4.png){#fig:004 width=70%}

4. Для построения полиномиальной кривой создадим векторы *x* и *y* (рис. @fig:005) и построим график (рис. @fig:006).

![Векторы х и у](image/5.png){#fig:005 width=60%}

![График $y = -0.8929 x^2 + 5.65 x - 4.4$](image/6.png){#fig:006 width=70%}

5. Для построения полиномальной кривой можно использовать встроенный метод *polyfit* (рис. @fig:007), В результате получаем такой график (рис. @fig:008).

![Метод Polyfit](image/7.png){#fig:007 width=70%}

![График Polyfit](image/8.png){#fig:008 width=70%}

## Матричные преобразования

Создадим матрицу данных и отдельные вектора *x* и *y* (рис. @fig:009), которые в графическом представлении имеют вид (рис. @fig:010).

![Исходные данные. Матрица и векторы](image/9.png){#fig:009 width=70%}

![Граф "домик"](image/10.png){#fig:010 width=70%}

### Вращение

Изучим, как осуществляется вращение изображения.

Зададим угол поворота и матрицу вращения, посчитаем новые координаты для угла 90 градусов (рис. @fig:011) и угла 225 градусов (рис. @fig:012). В результате получаем такую картинку (рис. @fig:013).

![Данные для поворота на 90 градусов](image/11.png){#fig:011 width=70%}

![Данные для поворота на 225 градусов](image/12.png){#fig:012 width=70%}

![Результат поворота](image/13.png){#fig:013 width=60%}

### Отражение

Изучим, как осуществляется отражение изображения относительно прямой.

Зададим матрицу отражения относительно прямой $x = y$, посчитаем новые координаты (рис. @fig:014). В результате получаем такую картинку (рис. @fig:015).

![Данные для отражения](image/14.png){#fig:014 width=70%}

![Результат отражения](image/15.png){#fig:015 width=70%}

### Дилатация

Изучим, как осуществляется дилатация (расширение или сжатие) изображения.

Зададим матрицу расширения в 2 раза, посчитаем новые координаты (рис. @fig:016). В результате получаем такую картинку (рис. @fig:017).

![Данные для расширения](image/16.png){#fig:016 width=70%}

![Результат расширения](image/17.png){#fig:017 width=70%}

# Выводы

Изучила подгонку полиномиальной прямой и матричные преобразования в Octave.
