 ![APM](https://img.shields.io/badge/python-2.7-green)  ![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

# ChainTimer

 ![ChainTimer](assets\ChainTimer.png)

1.  Задать время. Можно использовать такой формат:
   - 0.5 - задать секунды (50 секунд)
   - 0.1 - задать секунды (10 секунд)
   - 0.9 - задать секунды (1 минута 30 секунд)
   - 5.5 - задать 5 минут и 30 секунд (десятые задают время в процентах от 60,  т.е. 0.5 - это 50% от 60-ти)
2.  Выполненные циклы, отсчитываются, пока идёт таймер и не была нажата кнопка Stop (Start становится Stop во время отсчёта).
3. Оставшиеся циклы, если было указано количество циклов, которые нужно выполнить.
4.  Можно указать количество циклов, которое нужно выполнить.
5. Общее количество выполненных циклов.
6. Проработанное (job - работа, а не то, что вы подумали) в пустую время, отсчитывается, пока таймер не активирован и продолжает отсчитываться после нажатия кнопки Stop.

Таймер для отсчёта циклов с GUI интерфейсом. Можно для начала отсчёта устанавливать любое время, но циклы всегда считаются равными 25 минутам. Т.е. если вы установите 25 минут, то после окончания отсчёта будет выполнен один цикл. Так же даже после того, как отсчёт закончился, циклы продолжат считаться, пока не будет нажат "стоп". Таким образом, если вы погрузитесь в работу, то все равно сможете потом посмотреть, сколько циклов проработали.

Далее количество проработанных циклов можно использовать для статистики или просто включать таймер для концентрации внимания.
После истечения времени будет включен трек, помещённый в `ChainTimer/music/`. Если там аудиофайла нет, то звукового сигнала не будет.

### Как установить:

Ввиду того, что PyQt4 устарел и больше не поддерживается, установить его нужно следующим образом:

1. Перейти на сайт [Криса Голкена (Chris Golke)](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyqt4) и скачать соответствующую версию wheel packages для PyQt4. Имена файлов указаны таким образом, что часть названия  например `cp27` означает Python 2.7,  а `cp35` означает Python 3.5, и т.д.
2.  Далее прописать, подставив свой путь и скачанную версию:
   `C:\path\where\wheel\is\> pip install PyQt4‑4.11.4‑cp27‑cp27m‑win_amd64.whl`

Создайте и поместите `*.mp3` в директорию `ChainTimer/music/your_music.mp3`.