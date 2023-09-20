---
## Front matter
title: "Отчёт по индивидиуальному проекту. Этап №1"
subtitle: "Дисциплина: Научное программирование"
author: "Полиенко Анастасия Николаевна, НПМмд-02-23"

## Generic otions
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

Создание персонального научного сайта-визитки на основе системы управления статическими сайтами.

# Задание

Разместить на Github pages заготовки для персонального сайта.

# Ход работы

1. Создаём репозиторий *blog* на основе шаблона (рис. @fig:001).

![Репозиторий blog](image/1.png){#fig:001 width=70%}

1. Проверяем работу сайта на локальном сервере с помощью hugo server (рис. @fig:002).

![Сайт на локальном сервере](image/2.png){#fig:002 width=70%}

1. Создаём репозиторий *anpolienko.github.io* для размещения сайта на хостинге (рис. @fig:003).

![Репозиторий anpolienko.github.io](image/3.png){#fig:003 width=70%}

1. Создаём подмодуль в папке public (рис. @fig:004).

![Подмодуль public](image/4.png){#fig:004 width=70%}

1. Запускаем повторно hugo для создания сайта на публичном сервере (рис. @fig:005).

![Публичные файлы](image/5.png){#fig:005 width=70%}

# Выводы

Провела первый этап подготовки к созданию персонального научного сайта-визитки на основе системы управления статическими сайтами.
