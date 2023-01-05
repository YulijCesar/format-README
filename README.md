# Описание разметки файла README.md
Для описания проектов на GitHub используется README.md, который пишется на языке разметки markdown. Что и как поддерживается расписано ниже. Также существует еще один формат - [reStructuredText](https://github.com/GnuriaN/format-README/blob/master/README.rst), описание которого вынесено в отдельный файл `README.rst`.

## Оглавление
#подзаголовок
0. [Разделительная черта](#Разделительная-черта)
1. [Заголовки](#Заголовки)
2. [Работа с выделением текста](#Работа-с-выделением-текста)
3. [Использование эмодзи (emoji)](#Использование-эмодзи-emoji)
4. [Использование цитирования в тексте](#Использование-цитирования-в-тексте)
5. [Подсветка кода](#Подсветка-кода)
6. [Списки](#Списки)
    1. [Маркированный](#Маркированный)
    2. [Нумерованный](#Нумерованный)
    3. [Смешанные списки](#Смешанные-списки)
    4. [Список задач](#Список-задач)
7. [Ссылки](#Ссылки)
8. [Вставка изображения](#Вставка-изображения)
9. [Вставка таблиц](#Вставка-таблиц)
10. [Диаграмм Mermaid.js](#диаграмм-mermaidjs)
11. [Дополнения](https://github.com/GnuriaN/format-README/blob/master/Дополнения.md)
    
## Разделительная черта
При использовании
```
____
```
получается разделительная черта
____
[:arrow_up:Оглавление](#Оглавление)
___
## Заголовки

Всего существует шесть уровней заголовков. Для того, чтобы создать заголовок, необходимо в начале строки добавить символы `#`, в количестве равном его уровню.
____
# Заголовок первого уровня
```
# Заголовок 1
```
Заголовок первого уровня также можно создать:
```
Заголовок 1
===========
```
____
## Заголовок второго уровня
```
## Заголовок 2
```
Заголовок второго уровня также можно создать:
```
Заголовок 2
-----------
```
____
### Заголовок третьего уровня
```
### Заголовок 3
```
____
#### Заголовок четвертого уровня
```
#### Заголовок 4
```
____
##### Заголовок пятого уровня
```
##### Заголовок 5
```
____
###### Заголовок шестого уровня
```
###### Заголовок 6
```
____
[:arrow_up:Оглавление](#Оглавление)
____
## Работа с выделением текста

```
~~Зачеркнутый текст~~
```
~~Зачеркнутый текст (Strikethrough)~~

Для выделения текста **`жирным`** или *`наклонным`* и их сочетания можно использовать комбинации `*` или `_`

```
**Жирный текст (bold)**
```
**Жирный текст (bold)**

```
*Наклонный текст (italic)*
```
*Наклонный текст (italic)*

```
***Жирный наклонный текст (bold italic)***
```
***Жирный наклонный текст (bold italic)***

```
__Жирный текст (bold)__
```
__Жирный текст (bold)__

```
_Наклонный текст (italic)_
```
_Наклонный текст (italic)_

```
___Жирный наклонный текст (bold italic)___
```
___Жирный наклонный текст (bold italic)___

```
~~*__Тут странный текст__*~~
```
~~*__Тут странный текст__*~~
    
[:arrow_up:Оглавление](#Оглавление)
____
## Использование эмодзи (emoji)
В самом тексте можно использовать эмодзи, например написать вот так:    
:white_check_mark: Это уже сделано    
:negative_squared_cross_mark: Я не буду это делать    
:black_square_button: делать или не делать, вот в чем вопрос?    
В оригинале это выглядит так (в конце строки четыре (4) пробела для того, что бы был переход на новую строку):
```
:white_check_mark: Это уже сделано    
:negative_squared_cross_mark: Я не буду это делать    
:black_square_button: делать или не делать, вот в чем вопрос?    
```

Список работающих Эмодзи находится тут -> [emoji.md](https://github.com/GnuriaN/format-README.md/blob/master/emoji.md)    
    
[:arrow_up:Оглавление](#Оглавление)
___
## Использование цитирования в тексте
```
> Цитата (уровень 1)    
> > Вложенная цитата (уровень 2)    
> > > Вложенная цитата (уровень 3)    

> > Продолжение цитаты (уровень 2)    

> Продолжение цитаты (уровень 1)    
```
> Цитата (уровень 1)    
> > Вложенная цитата (уровень 2)    
> > > Вложенная цитата (уровень 3)    

> > Продолжение цитаты (уровень 2)    

> Продолжение цитаты (уровень 1)    

Внешний вид, конечно, не очень, но может и пригодиться.

[:arrow_up:Оглавление](#Оглавление)
___
## Подсветка кода

Если нужно выделить слово или фразу внутри строки, то используются одинарные обратные кавычки (`):

    Это `слово` будет выделено

Для выделения в блоки - тройные:

    ```
        Здесь может быть
        Ваша реклама
    ```

Дополнительно можно задавать язык кода внутри блока, указав его после первых трех кавычек:

    ```html
        <input type="text">
    ```

    ```css
        body {
            margin: 0;
            padding: 0;
        }
    ```

    ```php
        <?php phpinfo();?>
    ```

Пример блока для `C#`:

```C#
using MarkdownSharp;
using MarkdownSharp.Extensions.Mal;

Markdown mark = new Markdown();

// Short link for MAL - 
// http://myanimelist.net/people/413/Kitamura_Eri => mal://Kitamura_Eri
mark.AddExtension(new Articles()); 
mark.AddExtension(new Profile());

mark.Transform(text);
```

Пример блока для `Python`:
```Python
from timeit import Timer

tmp = "Python 3.2.2 (default, Jun 12 2011, 15:08:59) [MSC v.1500 32 bit (Intel)] on win32."

def case1(): # А. инкрементальные конкатенации в цикле
    s = ""
    for i in range(10000):
        s += tmp

def case2(): # Б. через промежуточный список и метод join
    s = []
    for i in range(10000):
        s.append(tmp)
    s = "".join(s)

def case3(): # В. списковое выражение и метод join
    return "".join([tmp for i in range(10000)])

def case4(): # Г. генераторное выражение и метод join
    return "".join(tmp for i in range(10000))

for v in range(1,5):
    print (Timer("func()","from __main__ import case%s as func" % v).timeit(200))
```
    
[:arrow_up:Оглавление](#Оглавление)
___
## Списки

#### Маркированный
Задать **маркированный** список можно несколькими символами `-`, `+` или `*`:
```
- Уровень списка 1. Пункт 1.
- Уровень списка 1. Пункт 2.
- Уровень списка 1. Пункт 3.
```
- Уровень списка 1. Пункт 1.
- Уровень списка 1. Пункт 2.
- Уровень списка 1. Пункт 3.

```
+ Уровень списка 1. Пункт 1.
+ Уровень списка 1. Пункт 2.
+ Уровень списка 1. Пункт 3.
```
+ Уровень списка 1. Пункт 1.
+ Уровень списка 1. Пункт 2.
+ Уровень списка 1. Пункт 3.

```
* Уровень списка 1. Пункт 1.
* Уровень списка 1. Пункт 2.
* Уровень списка 1. Пункт 3.
```
* Уровень списка 1. Пункт 1.
* Уровень списка 1. Пункт 2.
* Уровень списка 1. Пункт 3.

Можно создавать многоуровневые списки. Каждый уровень отделяется **четырьмя** (4) пробелами:
```
- Уровень списка 1. Пункт 1.
    - Уровень списка 2. Пункт 1.
- Уровень списка 1. Пункт 2.
    - Уровень списка 2. Пункт 1.
    - Уровень списка 2. Пункт 2.
- Уровень списка 1. Пункт 3.
    - Уровень списка 2. Пункт 1.
        - Уровень списка 3. Пункт 1.
        - Уровень списка 3. Пункт 2.
           - Уровень списка 4. Пункт 1.
```
- Уровень списка 1. Пункт 1.
  - Уровень списка 2. Пункт 1.
- Уровень списка 1. Пункт 2.
    - Уровень списка 2. Пункт 1.
    - Уровень списка 2. Пункт 2.
- Уровень списка 1. Пункт 3.
    - Уровень списка 2. Пункт 1.
      - Уровень списка 3. Пункт 1.
      - Уровень списка 3. Пункт 2.
         - Уровень списка 4. Пункт 1.

Каждый уровень отделяется двумя пробелами.

#### Нумерованный
Для Githib работа с нумерованными списками выглядит очень интересно. Каждый уровень отделяется **четырьмя** (4) пробелами:
```
1. Первый уровень 1
    1. Второй уровень 1
        1. Третий уровень 1
            1. Четвертый уровень 1
                1. Пятый уровень 1
                    1. Шестой уровень
                        1. Седьмой уровень
                            1. Седьмой уровень
2. Первый уровень 2
2. Первый уровень (должно быть 3)
4. Первый уровень 4
```
1. Первый уровень 1
    1. Второй уровень 1
        1. Третий уровень 1
            1. Четвертый уровень 1
                1. Пятый уровень 1
                    1. Шестой уровень
                        1. Седьмой уровень
                            1. Седьмой уровень
2. Первый уровень 2
2. Первый уровень (должно быть 3)
4. Первый уровень 4

#### Смешанные списки
При использовании смешанных списков нужно очень внимательно следить за нумерацией. Лучше, как и в нумерованных, использовать четыре (4) пробела для отделения уровня.
```
1. Первый уровень "нумерованный" - 1
    * Второй уровень "маркер"
        + Третий уровень "маркер"
        - Третий уровень "маркер"
        1. Третий уровень "нумерованный" - 1
            1. Четвертый уровень "нумерованный" - 1
                1. Пятый уровень "нумерованный" - 1
                    1. Шестой уровень "нумерованный" - 1
                        1. Седьмой уровень "нумерованный" - 1
                        * Седьмой уровень "маркер"
                        2. Седьмой уровень "нумерованный" - 1 (нарушена нумерация, новая нумерация 1)
                        3. Седьмой уровень "нумерованный" - 1 (нарушена нумерация, новая нумерация 2)
                            1. Восьмой уровень "нумерованный" - 1
2. Первый уровень "нумерованный" - 2
- Первый уровень "нумерованный" - 3
4. Первый уровень "нумерованный" - 4 (нарушена нумерация, новая нумерация 1)
5. Первый уровень "нумерованный" - 5 (нарушена нумерация, новая нумерация 2)
```
1. Первый уровень "нумерованный" - 1
    * Второй уровень "маркер"
        + Третий уровень "маркер"
        - Третий уровень "маркер"
        1. Третий уровень "нумерованный" - 1
            1. Четвертый уровень "нумерованный" - 1
                1. Пятый уровень "нумерованный" - 1
                    1. Шестой уровень "нумерованный" - 1
                        1. Седьмой уровень "нумерованный" - 1
                        * Седьмой уровень "маркер"
                        2. Седьмой уровень "нумерованный" - 2
                        3. Седьмой уровень "нумерованный" - 3
                            1. Восьмой уровень "нумерованный" - 1
2. Первый уровень "нумерованный" - 2
- Первый уровень "маркерный" - 3
4. Первый уровень "нумерованный" - 4 (хотя по идее должен быть 3)
5. Первый уровень "нумерованный" - 5 (хотя, по идее должен быть 3)

#### Список задач
(Task List)
Можно создавать "Списки задач" для этого необходимо использовать `- [ ]` для поставленной задачи и `- [X]` для выполненной задачи.
```
- [X] Придумать внешний вид резюме
- [ ] Написать основные категории
- [X] Опубликовать

```
- [X] Придумать внешний вид резюме
- [ ] Написать основные категории
- [X] Опубликовать

Также можно создавать многоуровневые списки задач. Каждый уровень отделяется **четырьмя** (4) пробелами:
```
- [X] Задача 1
    - [X] Подзадача 1 для Задачи 1
    - [X] Подзадача 2 для Задачи 1
- [ ] Задача 2
    - [X] Подзадача 1 для Задачи 2
    - [ ] Подзадача 2 для Задачи 2
- [ ] Задача 3
    - [ ] Подзадача 1 для Задачи 3
        - [ ] Подзадача 1 для Подзадача 1 для Задачи 3
```
- [X] Задача 1
    - [X] Подзадача 1 для Задачи 1
    - [X] Подзадача 2 для Задачи 1
- [ ] Задача 2
    - [X] Подзадача 1 для Задачи 2
    - [ ] Подзадача 2 для Задачи 2
- [ ] Задача 3
    - [ ] Подзадача 1 для Задачи 3
        - [ ] Подзадача 1 для Подзадача 1 для Задачи 3
    
[:arrow_up:Оглавление](#Оглавление) 
___
## Ссылки
Либо просто вставить ссылку, либо дополнительно задать текст ссылки (пробела между скобками быть не должно):
```
Первый вариант вставки ссылок - это просто написать адрес сайта http://sabaka.net
```
Первый вариант вставки ссылок - это просто написать адрес сайта http://sabaka.net

Второй вариант записывается так: `[текст ссылки](адрес ссылки)`
```
[sabaka.net](http://sabaka.net)
```
[sabaka.net](http://sabaka.net)
    
[Sabaka(DOT)Net]:http://sabaka.net    
    
[:arrow_up:Оглавление](#Оглавление)
____
## Вставка изображения
```
![Alt-текст](https://avatars1.githubusercontent.com/u/5384215?v=3&s=460 "Орк")
```
![Alt-текст](https://avatars1.githubusercontent.com/u/5384215?v=3&s=460 "Орк")

### Дополнительно:
#### Вставка ссылки с картинкой на ролик с YouTube
Описание комбинации `[![Тут текст](адрес до картинки)](ссылка на страничку YouTube)`        
Пример:        
```[![Тут текст](https://img.youtube.com/vi/RHPYGwVQB2o/0.jpg)](https://youtu.be/RHPYGwVQB2o)```        
Что мы увидим:        
[![Тут текст](https://img.youtube.com/vi/RHPYGwVQB2o/0.jpg)](https://youtu.be/RHPYGwVQB2o)        
        
[:arrow_up:Оглавление](#Оглавление) 
____
## Вставка таблиц
```
| LEFT | CENTER | RIGHT |
|----------------|:---------:|----------------:|
| По левому краю | По центру | По правому краю |
| текст | текст | текст |
```
| LEFT | CENTER | RIGHT |
|----------------|:---------:|----------------:|
| По левому краю | По центру | По правому краю |
| текст | текст | текст |

**Внимание:** Если в тексте таблицы нужно использовать символ "вертикальная черта - `|`", то в место него необходимо написать замену на комбинацию HTML-кода* `&#124;`, это нужно для того, что бы таблица не потеряла ориентации.    
*) - Можно использовать ASCII и/или UTF коды.

**Пример:**
```
| Обозначение | Описание | Пример регулярного выражения|
|----:|:----:|:----------|
| literal | Строка содержит символьный литерал literal | foo |
| re1&#124;re2 | Строка содержит регулярные выражения `rel` или `re2` | foo&#124;bar |
```
**Результат:**

| Обозначение | Описание | Пример регулярного выражения|
|----:|:----:|:----------|
| literal | Строка содержит символьный литерал literal | foo |
| re1&#124;re2 | Строка содержит регулярные выражения `rel` или `re2` | foo&#124;bar |

[:arrow_up:Оглавление](#Оглавление) 
____
## Диаграмм Mermaid.js
Появилась возможность вставлять диаграммы [Mermaid.js](https://mermaid-js.github.io/mermaid/#/)

<pre>
```mermaid
... код диаграммы ...
```
</pre>
Пример:
<pre>
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```
</pre>
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```
Очень подробно на русском языке о диаграммах Mermaid.js: https://habr.com/ru/post/652867/ 

[:arrow_up:Оглавление](#Оглавление) 
____
