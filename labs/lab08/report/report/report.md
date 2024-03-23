---
## Front matter
title: "Отчёта по лабораторной работе"
subtitle: "Лабораторная работа №8"
author: "Диана Садова Алексеевна"

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
lot: true # List of tables
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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных. Приобретение практических навыков: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.

# Последовательность выполнения работы

1)Осуществите вход в систему, используя соответствующее имя пользователя.(рис. [-@fig:001]).

![Вход в систему](image/1.png){#fig:001 width=90%}

Мы вошли в систему и можем продолжить работу

2) Запишите в файл file.txt названия файлов, содержащихся в каталоге /etc. Допишите в этот же файл названия файлов, содержащихся в вашем домашнем каталоге.(рис. [-@fig:002]).

![Создали файл и почестили в него имена файлов и каталогов домашнего каталога и /etc](image/2.1.png){#fig:002 width=90%}

3) Выведите имена всех файлов из file.txt, имеющих расширение .conf, после чего запишите их в новый текстовой файл conf.txt.(рис. [-@fig:003]).

![Перемещаем файлы с .conf в отдельный файл](image/3.png){#fig:003 width=90%}

4) Определите, какие файлы в вашем домашнем каталоге имеют имена, начинавшиеся с символа c? Предложите несколько вариантов, как это сделать.(рис. [-@fig:004]),(рис. [-@fig:005]).

![Выводим файлы начинавшиеся с символа c](image/4.png){#fig:004 width=90%}

![Выводим файлы начинавшиеся с символа t](image/4.1.png){#fig:005 width=90%}

5) Выведите на экран (по странично) имена файлов из каталога /etc, начинающиеся с символа h.(рис. [-@fig:006]).

![Выводим файлы начинавшиеся с символа h](image/5.png){#fig:006 width=90%}

6) Запустите в фоновом режиме процесс, который будет записывать в файл ~/logfile файлы, имена которых начинаются с log.(рис. [-@fig:007]).

![Запускаем в фоновом режиме процесс записи файлов в файл ~/logfile](image/6.png){#fig:007 width=90%}

7) Удалите файл ~/logfile.(рис. [-@fig:008]).

![Удаляем файл ~/logfile](image/7.png){#fig:008 width=90%}

8) Запустите из консоли в фоновом режиме редактор gedit.(рис. [-@fig:009]).

![Запускаем редактор gedit](image/8.png){#fig:009 width=90%}

9) Определите идентификатор процесса gedit, используя команду ps, конвейер и фильтр grep. Как ещё можно определить идентификатор процесса?(рис. [-@fig:010]).

![Определяем идентификатор процесса gedit](image/9.png){#fig:010 width=90%}

10) Прочтите справку (man) команды kill, после чего используйте её для завершения процесса gedit.(рис. [-@fig:011]),(рис. [-@fig:012]),(рис. [-@fig:013]).

![Читаем про каманду kill](image/10.1.png){#fig:011 width=90%}

![Узнаем намер процеса gedit](image/10.2.png){#fig:012 width=90%}

![Применяем каманду kill к gedit](image/10.3.png){#fig:013 width=90%}

11) Выполните команды df и du, предварительно получив более подробную информацию об этих командах, с помощью команды man.(рис. [-@fig:014]),(рис. [-@fig:015]),(рис. [-@fig:016]),(рис. [-@fig:017]).

![Читаем про каманду df](image/11.1.png){#fig:014 width=90%}

![Читаем про каманду du](image/11.2.png){#fig:015 width=90%}

![Используем каманду df](image/11.3.png){#fig:016 width=90%}

![Используем каманду du](image/11.4.png){#fig:017 width=90%}

12) Воспользовавшись справкой команды find, выведите имена всех директорий, имеющихся в вашем домашнем каталоге.(рис. [-@fig:018]),(рис. [-@fig:019]),(рис. [-@fig:020]).

![Читаем про каманду find](image/12.1.png){#fig:018 width=90%}

![Применяем каманду](image/12.2.png){#fig:019 width=90%}

![Результат](image/12.3.png){#fig:020 width=90%}

# Выводы

Ознакомились с инструментами поиска файлов и фильтрации текстовых данных. Приобрели практические навыки: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.

# Список литературы{.unnumbered}

::: {#refs}
:::
