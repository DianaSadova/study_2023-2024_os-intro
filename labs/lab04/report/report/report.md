---
## Front matter
title: "Отчёта по лабораторной работе"
subtitle: "Лабораторная работа №4"
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

Получение навыков правильной работы с репозиториями git.

# Задание

1) Выполнить работу для тестового репозитория.

2) Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional commits.

# Последовательность выполнения работы

## Установка программного обеспечения

### Установка git-flow

Linux

	Fedora
	
		Установка из коллекции репозиториев Copr (https://copr.fedorainfracloud.org/coprs/elegos/gitflow/):(рис. [-@fig:001]),(рис. [-@fig:002]).

![Устонавливаем коллекции репозиториев Copr](image/1.png){#fig:001 width=90%}

![Установка gitflow](image/2.png){#fig:002 width=90%}

После завершения этих програм можем двигатся дальше

### Установка Node.js

На Node.js базируется программное обеспечение для семантического версионирования и общепринятых коммитов. (рис. [-@fig:003]),(рис. [-@fig:004]).

	Fedora
	
![Установка nodejs](image/3.png){#fig:003 width=90%}

![Установка pnpm](image/4.png){#fig:004 width=90%}

Установка этих систем позволит выполнить данную лабораторную

### Настройка Node.js

Для работы с Node.js добавим каталог с исполняемыми файлами, устанавливаемыми yarn, в переменную PATH.

    Запустите:(рис. [-@fig:005]).

![Добавление каталога с исполняемыми файлами](image/5.png){#fig:005 width=90%}

    Перелогиньтесь, или выполните:(рис. [-@fig:006]).

![Выполняем программу source ~/.bashrc](image/6.png){#fig:006 width=90%}

### Общепринятые коммиты

    1)commitizen

        Данная программа используется для помощи в форматировании коммитов.(рис. [-@fig:007]).

![Добавляем программу для форматирования коммитов](image/7.png){#fig:007 width=90%}

        При этом устанавливается скрипт git-cz, который мы и будем использовать для коммитов.
 
После завершения установки переходим к пункту 2

    2)standard-changelog

        Данная программа используется для помощи в создании логов.(рис. [-@fig:008]).

![Добавляем программу для помощи в создании логов](image/8.png){#fig:008 width=90%}

После завершения установки переходим к пункту 3

    3)Практический сценарий использования git

        1.Создание репозитория git

            1.Подключение репозитория к github

                Создайте репозиторий на GitHub. Для примера назовём его git-extended.рис. [-@fig:009]).

![Создаем новый репридиторий с именем git-extended](image/9.png){#fig:009 width=90%}

                Делаем первый коммит и выкладываем на github:(рис. [-@fig:010]).

![Делаем коммит и отправляем на github](image/10.png){#fig:010 width=90%}

Для данного действия, я клонировала наш новый репридиторий и создала в нем файл README.md

            2.Конфигурация общепринятых коммитов

                Конфигурация для пакетов Node.js(рис. [-@fig:011]).

![Подключаем конфигурацию для пакетов Node.js](image/13.png){#fig:011 width=90%}

                Необходимо заполнить несколько параметров пакета.
                    Название пакета.
                    Лицензия пакета. Список лицензий для npm: https://spdx.org/licenses/. Предлагается выбирать лицензию CC-BY-4.0.

                Сконфигурим формат коммитов. Для этого добавим в файл package.json команду для формирования коммитов:

                Таким образом, файл package.json приобретает вид:(рис. [-@fig:012]).

![Переписываем файл package.json](image/11.png){#fig:012 width=90%}

Данная процедура нам поможет при дальнейшей работе

                Добавим новые файлы:(рис. [-@fig:013]).

![Добавляем новые файлы](image/12.png){#fig:013 width=90%}

                Выполним коммит:(рис. [-@fig:014]).

![Выполняем коммит](image/14.png){#fig:014 width=90%}

Выполняем коммит для нового файла

                Отправим на github:(рис. [-@fig:015]).

![Отправляем файл на github](image/15.png){#fig:015 width=90%}

            3.Конфигурация git-flow

                Инициализируем git-flow(рис. [-@fig:016]).

![Изменяем конфигурацию git-flow](image/16.png){#fig:016 width=90%}

                Префикс для ярлыков установим в v.

                Проверьте, что Вы на ветке develop:(рис. [-@fig:017]).

![Проверяем, что мы на ветке develop](image/17.png){#fig:017 width=90%}

Убедились, что мы на нужной ветке, ведь в последствии она нам понадобится 

                Загрузите весь репозиторий в хранилище:(рис. [-@fig:018]).

![Загружаем репозиторий в хранилище](image/18.png){#fig:018 width=90%}

                Установите внешнюю ветку как вышестоящую для этой ветки:(рис. [-@fig:019]).

![Установливаем внешнюю ветку](image/19.png){#fig:019 width=90%}

                Создадим релиз с версией 1.0.0(рис. [-@fig:020]).

![Создаем релиз версии 1.0.0](image/20.png){#fig:020 width=90%}

                Создадим журнал изменений(рис. [-@fig:021]).

![Создаем журнал изменений](image/21.png){#fig:021 width=90%}

Что бы воспользоваься программой standard-changelog нужно было ее сначало установить (проверенно на собственном опыте)

                Добавим журнал изменений в индекс(рис. [-@fig:022]).

![Добавляем в индекс журнал изменений](image/22.png){#fig:022 width=90%}

                Зальём релизную ветку в основную ветку(рис. [-@fig:023]).

![Загружаем релизную ветку в основную ветку](image/23.png){#fig:023 width=90%}

                Отправим данные на github(рис. [-@fig:024]),(рис. [-@fig:025]).

![Отправляем данные на github](image/24.png){#fig:024 width=90%}

![Отправляем данные на github](image/25.png){#fig:025 width=90%}

                Создадим релиз на github. Для этого будем использовать утилиты работы с github:(рис. [-@fig:026]).

![Создаем релиз на github](image/26.png){#fig:026 width=90%}

        2.Работа с репозиторием git

            1.Разработка новой функциональности

                Создадим ветку для новой функциональности:(рис. [-@fig:027]).

![Создадим новую ветку](image/27.png){#fig:027 width=90%}

                Далее, продолжаем работу c git как обычно.

                По окончании разработки новой функциональности следующим шагом следует объединить ветку feature_branch c develop:(рис. [-@fig:028]).

![ОбЪединяем две ветки](image/28.png){#fig:028 width=90%}

            2.Создание релиза git-flow

                Создадим релиз с версией 1.2.3:(рис. [-@fig:030]).

![Создаем новый релиз с версией 1.2.3](image/30.png){#fig:030 width=90%}

                Обновите номер версии в файле package.json. Установите её в 1.2.3.,(рис. [-@fig:029]).

![Обновляем номер версии в файле package.json](image/29.png){#fig:029 width=90%}

Нам понадобится это обновление, так как без него не будут работать следующие программы

                Создадим журнал изменений(рис. [-@fig:031]).

![Создаем новый журнал изменений](image/31.png){#fig:031 width=90%}

                Добавим журнал изменений в индекс(рис. [-@fig:032]),(рис. [-@fig:033]).

![Добавляем в индекс журнал изменений](image/32.1.png){#fig:032 width=90%}

![Добавляем в индекс журнал изменений](image/32.2.png){#fig:033 width=90%}

                Зальём релизную ветку в основную ветку(рис. [-@fig:034]).

![Загружаем релизную ветку в основную ветку](image/33.png){#fig:034 width=90%}

                Отправим данные на github(рис. [-@fig:035]),(рис. [-@fig:036]).

![Отправляем данные на github](image/34.png){#fig:035 width=90%}

![Отправляем данные на github](image/35.png){#fig:036 width=90%}

                Создадим релиз на github с комментарием из журнала изменений:(рис. [-@fig:037]).

![Создаем новый релиз на github](image/36.png){#fig:037 width=90%}

# Выводы

Получили навыки правильной работы с репозиториями git и освоили новые способы работы с ним

# Список литературы{.unnumbered}

::: {#refs}
:::
