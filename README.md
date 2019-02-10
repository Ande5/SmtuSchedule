[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
# Расписание «СПбГМТУ»
Мобильное приложение, которое знает расписание занятий любой группы, любого преподавателя в любой день семестра.
- Расписания загружаются прямо с сайта Корабелки;
- Загрузить можно сколько угодно много расписаний, хоть все;
- Быстрый переход между расписаниями с сохранением просматриваемой даты;
- Выводятся только занятия, которые будут в данный конкретный день (с учетом недели: числитель/знаменатель).
## Скриншоты
![](https://raw.githubusercontent.com/shults-s/SmtuSchedule/Screenshots/master/All.png)
## Установка и настройка
- В настройках смартфона разрешить установку приложений из неизвестных источников (на данном этапе, пока непонятно насколько это приложение нужно кому-то кроме меня, нет смысла выкладывать его в Google Play);
- Загрузить [последнюю версию](https://github.com/shults-s/SmtuSchedule/releases) установочного APK-файла и запустить его;
- По окончанию установки открыть приложение и в его настройках задать значение параметра «Первый день семестра по числителю».
## Совместимость
Поддерживаются все смартфоны на Android начиная с версии 5.1 и заканчивая 9.0 (самая современная на данный момент). Поддержки iOS нет, и, скорее всего, не будет.
## Редактирование расписаний
При первом запуске приложение создает во внутренней памяти смартфона директорию с названием «Расписание СПбГМТУ». Все загружаемые в дальнейшем с сайта расписания хранятся в этой директории в виде текстовых файлов в формате [JSON](https://ru.wikipedia.org/wiki/JSON). Их можно скопировать на компьютер, отредактировать, а затем закинуть обратно на смартфон. После перезапуска приложения изменения вступят в силу. Простейшее изменение, которое можно внести в расписание – это скрыть предмет. Для этого достаточно поменять значение параметра IsDisplayed с «true» на «false». После внесения изменений код желательно проверить валидатором (например, [этим](https://jsonlint.com/)) на предмет синтаксических ошибок. Расписания с ошибками приложение не открывает, о чем выводит соответствующее уведомление.
## Обратная связь
Свои пожелания, вопросы, сообщения об ошибках и прочее можно написать [мне в личку](https://vk.com/shults_s).\
Если приложение вылетело прошу подробно описывать предшествовавшие этому события. Во всех же остальных нештатных ситуациях оно записывает файл с отладочной информацией в директорию Logs, которая находится внутри директории приложения. Этот файл желательно приложить к сообщению об ошибке. Он не содержит никакой приватной информации, кроме модели устройства и версии Android.
## О проекте
Разработка заняла четыре месяца. Сейчас проект состоит из 2356 строк кода и еще 586 строк разметки, стилей и ресурсов интерфейса. Приложение написано на языке C# с использованием библиотеки Xamarin.Android. Отдельная благодарность разработчикам библиотек [Json.NET](https://www.newtonsoft.com/json) и [HtmlAgilityPack](https://html-agility-pack.net).\
Это мой первый опыт в мобильной разработке, поэтому далеко не все реализовано корректно, особенно по части фрагментов и UI в целом.