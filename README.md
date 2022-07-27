# png-file-processing
Обработка PNG файлов на C

## Задание:
Программа должна реализовывать весь следующий функционал по обработке
png-файла

Общие сведения
- Формат картинки PNG (рекомендуем использовать библиотеку libpng)
- без сжатия
- файл всегда соответствует формату PNG
- обратите внимание на выравнивание; мусорные данные, если их
необходимо дописать в файл для выравнивания, должны быть нулями.
- все поля стандартных PNG заголовков в выходном файле должны иметь
те же значения что и во входном (разумеется кроме тех, которые должны
быть изменены).

Программа должна реализовывать следующий функционал по обработке
PNG-файла
1. Рисование окружности. Окружность определяется:
либо координатами левого верхнего и правого нижнего угла квадрата, в который
она вписана, либо координатами ее центра и радиусом
толщиной линии окружности
цветом линии окружности. Окружность может быть залитой или нет
цветом которым залита сама окружность, если пользователем выбрана залитая
окружность
2. Фильтр rgb-компонент. Этот инструмент должен позволять для всего
изображения либо установить в 0 либо установить в 255 значение заданной
компоненты. Функционал определяется
Какую компоненту требуется изменить
В какой значение ее требуется изменить
3. Разделяет изображение на N*M частей. Реализация: либо провести линии
заданной толщины, тем самым разделив изображение либо сохранение каждой
части в отдельный файл. -- по желанию студента (можно и оба варианта).

Функционал определяется:
- Количество частей по “оси” Y
- Количество частей по “оси” X
- Толщина линии
- Цвет линии
- Либо путь куда сохранить кусочки

## Аннотация
В курсовой работе реализована обработка PNG файлов с использованием
библиотеки libpng. Реализованные опции обработки файла соответствуют
заданиям.

Использовалось несколько стандартных библиотек: stdio.h, stdlib.h,
getopt.h, string.h, math.h, unistd.h, stdarg.h. Программа реализована в виде
утилиты, подобной стандартным linux утилитам: управление осуществляется
посредством аргументов командной строки.

Инструкция компиляции и запуску приложения: скомпилировать файл
main.c из папки, в которой он находится, командой “gcc main.c -lpng -lm”.
Использовать ключи, описанные в справке (которую можно получить, вызвав
утилиту без аргументов или ключом -h (--help), -?).

## Заключение
В результате выполнения данной работы была на практике применена
библиотека libpng для работы с PNG-файлами и библиотека getopt для
построение консольного интерфейса. Была создана стабильная программа,
которая обрабатывает изображение в зависимости от команды пользователя.
Также произведена обработка всех возможных исключительных ситуаций.
