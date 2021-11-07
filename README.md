# Проекты Latex

<div style="page-break-after: always;"></div>

Содержание

<div style="page-break-after: always;"></div>

>1. [Документ](#document)<br/>
>>1.1. [Оформление глав](#chapters)<br/>
>>1.2. [Аббревиатура](#abbreviations)<br/>
>>1.3. [Список использованных источников](#bibliography)<br/>
>2. [Документ](#document-items)<br/>
>>2.1. [Списки](#lists)<br/>
>>2.2. [Рисунки](#figures)<br/>
>>2.3. [Таблицы](#tables)<br/>
>>2.4. [Ссылки](#links)<br/>
>3. [Стили](#styles)<br/>
>4. [Примеры](#examples)<br/>
>5. [Инструменты](#tools)<br/>
>>5.1. [Установка и использование под Ubuntu](#tools-ubuntu)<br/>
>>5.2. [Установка и использование под Windows](#tools-windows)<br/>
>>5.3. [Шрифты](#tool-fonts)<br/>

<div style="page-break-after: always;"></div>

## 1. Документ<a name="document"></a>

Ссылка на файл abbreviations:
```
\input{abbreviations}
```

### 1.1. Оформление глав<a name="chapters"></a>

Оформление главы:
```
\chapter{Глава 1}
\label{sec:part_name_1}
```

Пункт с указателем
```
\section{Пункт 1.1}
\label{sec:part_sec_name_1}
```

Подпункт с указателем
```
\subsection{Подпункт 1.1.1}
\label{sec:part_subsec_name_1}
```

Подподпункт с указателем
```
\subsubsection{Подпункт 1.1.1.1}
\label{sec:part_subsubsec_name_1}
```

### 1.2. Аббревиатура<a name="abbreviations"></a>

Главу "Аббревиатура" желательно сделать в отдельном файле. Ссылка на файл abbreviations:
```
\input{abbreviations}
```

Пример:
```
\Abbreviations

В настоящем документе применяют следующие термины с соответствующими определениями:
\begin{description}
\item [API] (программный интерфейс приложения, интерфейс прикладного программирования)
            (англ. application programming interface, API) — набор готовых классов, процедур, функций,
             структур и констант, предоставляемых приложением (библиотекой, сервисом) или
             операционной системой для использования во внешних программных продуктах.
\end{description}
```

### 1.3. Список использованных источников<a name="bibliography"></a>

Пример:
```
\begin{thebibliography}{9}

\bibitem{AMD_V}
AMD. Технология AMD-V™ для виртуализации клиентов.
 Web: \url{https://www.amd.com/ru/technologies/virtualization}

\bibitem{CERN_2018_KubeCon_pdf}
Презентация ЦЕРНа на KubeCon Europe 2018: Multi-Cloud Federated Kubernetes at CERN.
 Web: \url{https://schd.ws/hosted_files/kccnceu18/d0/CERN.pdf}

\end{thebibliography}
```

<div style="page-break-after: always;"></div>

## 2. Элементы документа<a name="document-items"></a>

### 2.1. Списки<a name="lists"></a>

```
    Далее мы перечисляем пункты:
    \begin{itemize}
    \item вариант 1;
    \item вариант 2;
    \item вариант 3.
    \end{itemize}
```

### Рисунки<a name="figures"></a>

30% от ширины страницы
```
    \begin{figure}[htp]
        \centering
        \includegraphics[width=0.3\textwidth]{file.png}
        \caption{Наименование рисунка}
        \label{fig:pic_link_name}
    \end{figure}
```
100% от ширины страницы
```
\begin{figure}[htp]
    \centering
  \includegraphics[width=\textwidth]{file.png}
    \caption{Наименование рисунка}
    \label{fig:pic_link_name}
\end{figure}
```

### Таблицы<a name="tables"></a>

Простая таблица:
```
\begin{sidewaystable}
  \caption{Перечень домов смарт-квартала}
  \label{table:table_houses}

\begin{tabular}{>{\centering\arraybackslash}m{3.5cm}|>{\arraybackslash}m{2cm}
   |>{\arraybackslash}m{2.4cm}|>{\arraybackslash}m{1.8cm}
   |>{\arraybackslash}m{2.2cm}|>{\arraybackslash}m{2.2cm}
   |>{\arraybackslash}m{2.2cm}|>{\arraybackslash}m{1.8cm}
   |>{\arraybackslash}m{2.5cm}|>{\arraybackslash}m{2.5cm}}

\hline
  Адрес & Общая площадь, кв.м. & Площадь жилых помещений, кв.м. & Проект &
   Год постройки & Этажность & Подъездов & Лифтов & Кол-во жилых помещений & Кол-во нежилых помещений \\ \hline
  Братиславская, д. 18 к. 1 & 35913.7 & 28307.2 & П-44/17 & 1998 & 18 & 8 & 16 & 512 & 21 \\ \hline
  Братиславская, д. 18 к. 2 & 21842 & 21327.5 & П-46М & 1997 & 12 & 11 & 22 & 331 & 5 \\ \hline
  Братиславская, д. 20 & 14032 & 10093.1 & КТЖС & 1998 & 22 & 2 & 6 & 152 & 2 \\ \hline
  Новомарьинская, д. 11 к. 1 & 15443.3 & 15408 & П-44 & 1996 & 14 & 5 & 10 & 278 & 2 \\ \hline
  Новомарьинская, д. 13 & 11208.4 & 11208.4 & П-44/17 & 1996 & 17 & 3 & 6 & 203 & 0 \\ \hline
  Мячковский б-р, д. 9 & 23959.3 & 23580.9 & П-44 & 1996 & 17 & 7 & 14 & 426 & 6 \\ \hline
  Мячковский б-р, д. 11 & 10107 & 9683.5 & КОПЭ & 1997 & 22 & 2 & 6 & 168 & 11 \\ \hline
  Итого: & 132505.7 & 119608.6 &  & 1996-1998 &  & 38 & 80 & 2070 & 47 \\ \hline
\end{tabular}

\end{sidewaystable}
```

Таблица будет повернута в альбомном формате:
```
\begin{landscape}
\begin{longtable}{ | m{4.5cm} | m{3.5cm} | m{4cm} | m{3cm} | crm{3.5cm} | }


   \caption{Пороговые значения показателей водоснабжения по каждому дому}
   \label{table_limits_water_metrics_house} \\

  Вид ресурса / системы & Наименование показателя & Период /способ предоставления данных & Ед.изм. &  В подающем трубопроводе \\ \hline\endhead

  \multicolumn{4}{l}{Центральное отопление (ЦО)}  &  \\ \hline
  Братиславская д.18 к.1 & тепловая энергия & каждые 30 минут & Гккал/час & 1.8442050000000001 \\ \hline
  Братиславская д.18 к.2 & тепловая энергия & каждые 30 минут & Гккал/час & 1.9518 \\ \hline
  Братиславская д. 20 & тепловая энергия & каждые 30 минут & Гккал/час & 0.56999999999999995 \\ \hline
  Новомарьинская д.11к.1 & тепловая энергия & каждые 30 минут & Гккал/час & 1.1399999999999999 \\ \hline
  Новомарьинская д.13 & тепловая энергия & каждые 30 минут & Гккал/час & 0.79 \\ \hline
  Мячковский б-р д.9 & тепловая энергия & каждые 30 минут & Гккал/час & 1.67 \\ \hline
  Мячковский б-р д.11 & тепловая энергия & каждые 30 минут & Гккал/час & 0.79700000000000004 \\ \hline
  \multicolumn{4}{l}{Горячее водоснабжение (ГВС)} &  \\ \hline
  Братиславская д.18 к.1 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 249.90299999999999 \\ \hline
  Братиславская д.18 к.2 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 240.626 \\ \hline
  Братиславская д. 20 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 88 \\ \hline
  Новомарьинская д.11к.1 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 115.51 \\ \hline
  Новомарьинская д.13 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 88.286000000000001 \\ \hline
  Мячковский б-р д.9 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 179.74100000000001 \\ \hline
  Мячковский б-р д.11 & горячее водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 84.378 \\ \hline
  \multicolumn{4}{l}{Холодное водоснабжение (ХВС)} &  \\ \hline
  Братиславская д.18 к.1 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 149.71899999999999 \\ \hline
  Братиславская д.18 к.2 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 94.677000000000007 \\ \hline
  Братиславская д. 20 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 55.536999999999999 \\ \hline
  Новомарьинская д.11к.1 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 65.301000000000002 \\ \hline
  Новомарьинская д.13 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 52.581000000000003 \\ \hline
  Мячковский б-р д.9 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 102.97799999999999 \\ \hline
  Мячковский б-р д.11 & холодное водоснабжение & каждые 30 минут & Расчетное суточное потребление горячей воды м3/сут. & 40.71 \\ \hline

\end{longtable}
\end{landscape}
```

### Ссылки<a name="links"></a>

На рисунок:
```
(см. рис. \ref{fig:pic_link_name})
```
На таблицу:
```
(см. табл.\ref{table:table_houses})
```
Цитирование источника:
```
\cite{CERN_2018_KubeCon_pdf}
```
На URL адрес:
```
\url{http://digitaleconomy.space}
```

<div style="page-break-after: always;"></div>
## Стили<a name="styles"></a>

```
\textbf{Этот текст будет жирным}
```
<div style="page-break-after: always;"></div>
## Примеры<a name="examples"></a>

### Разбиение документа на файлы

Файл документа со ссылками на другие документы:
```
\chapter{Пользовательские интерфейсы внешних систем}

\include{ch-foreign-ui-wasteout}

\newpage
\include{ch-foreign-ui-vaisala}

\newpage
\include{ch-foreign-ui-mosvodokanal}
```

### Глава

Пример главы
```
\chapter{Система хранения данных}

Система ownCloud используется в качестве системы хранения данных.

\textbf{ownCloud} — это свободное и открытое веб-приложение для синхронизации данных, общего доступа к файлам и удалённого хранения документов в «облаке» \cite{wiki_owncloud}.

Доступны клиенты для синхронизации данных с ПК под управлением Windows, OS X или Linux и с мобильными устройствами на iOS и Android. Кроме того, сохранённые данные доступны через веб-интерфейс ownCloud в любом браузере.

Возможности системы хранения данных:
\begin{itemize}
\item Хранение файлов с использованием обычных структур каталогов, или с использованием WebDAV
\item Криптография
\item Синхронизация между клиентами под управлением Windows (Windows XP, Vista, 7 и 8), Mac OS X (10.6 и новее) или Linux
\end{itemize}

\section{Web-интерфейс}
\label{sec:part_web_owncloud}

Система доступна по адресу \url{http://disk.digitaleconomy.space}

\section{Мобильная версия}
\label{sec:part_mobile_owncloud}

В качестве мобильного приложения рекомендуется использовать приложение "ocloud для owncloud" (см. рис. \ref{fig:pic_OwnCloud_Mobile}).

\begin{figure}[htp]
    \centering
  \includegraphics[width=0.3\textwidth]{owncloud-mobile.png}
    \caption{Мобильное приложение}
    \label{fig:pic_OwnCloud_Mobile}
\end{figure}
```

# Инструменты<a name="tools"></a>

## Установка для ОС Ubuntu<a name="tool-ubuntu"></a>

Установка библиотек
```
sudo apt install texlive-xetex
sudo apt install python3-pygments
sudo apt install ttf-mscorefonts-installer scalable-cyrfonts-tex 
sudo apt install texlive-luatex
sudo apt install texlive-lang-cyrillic
```

Установка шрифтов
```
fc-cache -f -v
luaotfload-tool -u -f
```

Изменить настройки в TexMaker
```
add flag to xelatex and luatex: -shell-escape
```

<div style="page-break-after: always;"></div>
## Установка и использование под Windows<a name="tool-windows"></a>

Для работы в Windows необходимо установить следующие зависимости:

1. [dwimperl](http://dwimperl.com/windows.html)
2. [texlive](https://www.tug.org/texlive/windows.html)
3. [inkscape](https://inkscape.org/ru/download/)
4. [dia](http://dia-installer.de/)
5. [graphviz](http://www.graphviz.org/Download_windows.php)
6. [ghostscript](https://ghostscript.com/download/gsdnld.html)
7. [babun](http://babun.github.io/) — не обязательно.
8. [cmake](https://cmake.org/download/) — не обязательно при использовании
   `babun`, обязательно при работе без него. В случае с `babun` нужно
   использовать `pact install cmake`, а не самостоятельную установку из
   установщика на сайте. В любом случае необходимо либо иметь babun+make, либо
   babun+cmake, либо cmake.

   Внимание: CMake не собирает ничего сам, он генерирует скрипты для make (и
   ряда других программ), только он умеет использовать разные диалекты: nmake
   (из Visual Studio), mingw32-make, MSYS make, … Поэтому что‐то из этого нужно
   также установить. На данный момент сборка проверялась для `babun+cmake`,
   `babun+make` и просто нативного `cmake`. В последнем случае использовалась
   утилита `make` из пакета WinAVR, идентифицирующаяся как GNU make.
9. [python](https://www.python.org/downloads/windows/) — при использовании babun
   не нужно, он уже установлен там.

   После установки python установить его пакет pygments.

После установки всех зависимостей необходимо добавить их в $PATH. Установщики
некоторых (texlive, cmake и dwimperl) делают это сами (но, возможно, требуется
установка галочки), для остальных нужно редактировать реестр, либо изменять PATH
временно. В PATH помещаются каталоги, в которых находятся следующие файлы:
`inkscape.exe`, `dia.exe`, `dot.exe`, `python.exe`.

Ghostscript предоставляет файлы gswin32.exe и gswin32c.exe, однако для работы
нужно иметь файл gs.exe или gs.bat где‐то в $PATH. В случае с bat файл должен
выглядеть так:

```bat
@echo off
P:\ath\to\ghostscript\gswin32c.exe %*
```

(ВНИМАНИЕ: именно `gswin32c.exe`, не `gswin32.exe`.) Можно просто скопировать
`gswin32c.exe` в `gs.exe` и добавить каталог с ними в `$PATH`.

В случае использования python из babun вам дополнительно нужен в `$PATH`
`pygmentize.bat` следующего содержания:

```bat
@echo off
C:\Users\{user}\.babun\cygwin\bin\python2.7.exe C:\Users\{user}\.babun\cygwin\bin\pygmentize %*
```

(замените `{user}` на своего пользователя). Что нужно в случае использования
python без babun я не знаю, но исполняемый файл pygmentize должен быть
в `$PATH`.

После того, как `$PATH` станет содержать пути ко всем необходимым исполняемым
файлам можно будет использовать выбранную систему сборки для создания PDF‐файла.
В случае с babun+[c]make:

1. Откройте babun.
2. Войдите в каталог с проектом с помощью `cd /path/to/latex-g7-32`.
3. При использовании cmake:

   1. Создайте каталог build: `mkdir build`.
   2. Войдите в него: `cd build`.
   3. Соберите проект: `cmake .. && make`. PDF появится
      в `/path/to/latex-g7-32/build/rpz.pdf` (он же rpz.pdf в текущем каталоге).
   4. При изменении tex файлов и картинок/диаграмм/… можно собирать просто
      с помощью `make`.
   5. При *добавлении* файлов/картинок/диаграмм нужно опять использовать `cmake
      ..` перед `make`.
   6. Для очистки от сгенерированных файлов можно просто удалить каталог
      `build`.

   При использовании `make`:

   1. Проект (пере)собирается просто `make`. PDF появится
      в `/path/to/latex-g7-32/rpz.pdf`.
   2. Для очистки от сгенерированных файлов можно использовать `make clean`.
      Проверяйте их наличие с помощью `git status --ignored`, временные файлы не
      сконцентрированы в одном каталоге в этом случае.

Нативный CMake:

1. Откройте `cmd.exe`.
2. Войдите в каталог с проектом с помощью:

   1. `D:`, где `D:` — буква диска, на котором лежит проект. Данная часть
      предназначена для переключения текущего диска: в `cmd.exe` у каждого диска
      свой текущий каталог, текущий каталог `cmd.exe` является текущим каталогом
      текущего диска.

      Под `D:` здесь понимается буквально: “введите команду `D:` и нажмите
      ввод”.
   2. `cd D:\path\to\latex-g7-32`.

3. Создайте каталог `build`: `mkdir build`.
4. Войдите в него: `cd build`.
5. Запустите `cmake ..`. Т.к. в отличие от \*nix систем (cygwin (babun) можно
   считать относящимся к таковым в определённой степени) на Windows нет
   «стандартного make», то вполне возможно, что просто `cmake ..` сделает не то,
   что нужно. Для GNU make из WinAVR, использовавшегося автором нужно было
   использовать команду `cmake .. -G "Unix Makefiles"`. Список возможных
   генераторов можно получить либо [на сайте CMake][cgens], либо указав `cmake`
   заведомо несуществующий генератор: к примеру, `cmake -G
   xxx_nonexistent_generator_xxx` (внимание, поведение может измениться в новой
   версии CMake). На сайте информация предоставлена более подробно.
6. Запустите `make`. В зависимости от того, какой генератор есть у вас в системе
   вместо `make` может оказаться `nmake` (распространяется с Visual Studio,
   соответствует `cmake .. -G "NMake Makefiles"`) или `mingw32-make`
   (распространяется с компилятором mingw32, соответствует `cmake .. -G "MinGW
   Makefiles"`).

   PDF файл появится в текущем каталоге (т.е. `D:\path\to\latex-g7-32\build`)
   под названием `rpz.pdf`.

[cgens]: https://cmake.org/cmake/help/latest/manual/cmake-generators.7.html

<div style="page-break-after: always;"></div>

## Шрифты<a name="tool-fonts"></a>

В отчёте можно использовать свободный аналог Times New Roman - PT Astra, они находятся в репозитории в каталоге fonts.
На линуксе устанавливаются в `$HOME/.fonts/` затем выполнить команды `fc-cache -f -v` и `luaotfload-tool -u -f`.

На Windows шрифты нужно скопировать в каталог C:\Windows\Fonts и также желательно выполнить команду `fc-cache -f -v`, чтобы документ, использующий шрифты, быстрее компилировался.

Опции класса документа, устанавливающие шрифты:

1. При использовании XeLaTeX:

    1. `astra` (по умолчанию) — свободные шрифты Astra Sans, Astra Serif, Liberation Mono.
    2. `times` — Шрифты Times New Roman, Arial, Courier New. Необходимо, чтобы у вас был подписан лицензионный договор с правообладателем шрифтов — компанией Monotype Imaging Inc.
    3. `cm` — Шрифты CMU, которые обычно включены в TeX Live.

2. При использовании PdfLaTeX:

   1. `times` (по умолчанию) — шрифты из пакета cyrtimes: Nimbus Roman и Nimbus Sans.
   2. `pscyr` — шрифты из пакета pscyr: Antiqua PSCyr, Textbook PSCyr, ERKurier PSCyr.
   3. `cm` — шрифты CM, которые обычно включены в TeX Live.

Если какой-то шрифт не найден, то вместо него будет использоваться соответствующий шрифт CM.

Эти опции нужно задавать в `\documentclass`, например так: `\documentclass[utf8x, times, 14pt]{G7-32}`

