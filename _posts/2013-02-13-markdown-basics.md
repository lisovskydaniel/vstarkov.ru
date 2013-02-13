---
layout: post
title: Основы маркдауна
isNotTranslated: true
categories : [markdown, workspace]
---

Основы маркдауна
================================================================================

1. [Вступление](#intro)
1. [Заголовки](#headings)
2. [Форматирование текста](#text-formatting)
3. [Вставка ссылок и картинок](#links-n-images)
4. [Списки](#lists)
5. [Форматирование кода](#code)
6. [Цитаты](#cite)
7. [Обычный HTML](#html)

<h2 id="intro"><a href="#intro">
    Вступление
</a></h2>

Маркдаун — самое удобное и интуитивно понятное для редактирования текста,
что можно было встретить в интернете. Его используют СтекОверфлоу и Гитхаб, что
уже означают повсеместность формата.

Сам по себе, маркдаун это свод правил для форматирования текста и транслятор в
HTML. На данный момент трансляторов существует великое множество, все они
поддерживают оригинальный стандарт, но некоторые вносят в свои трансляторы
дополнительные возможности.

Например, [**Крамдаун**](http://kramdown.rubyforge.org/)
(используемый в джекиле) создал синтаксис для [списка определений](http://kramdown.rubyforge.org/syntax.html#definition-lists) `dl`; а **ГФМ** ([GitHub Flavored Markdown)](https://help.github.com/articles/github-flavored-markdown) взял на себя больше и ввёл много
крутых особенностей для создания более удобного сервиса.


[Джон Грубер](http://daringfireball.net/) создал этот инструмент и самый больший
интерес для нас представляют две страницы:

* [Основы маркдауна](http://daringfireball.net/projects/markdown/basics)
* [Синтаксис маркдауна](http://daringfireball.net/projects/markdown/syntax)

--------------------------------------------------------------------------------

*В этой статье, я постарался изложить своё видение на изучение основ маркдауна,
и то как я его запомнил.*

Код из статьи (её [**маркдаун-исходник**](https://raw.github.com/matmuchrapna-sites/vstarkov.ru/gh-pages/_posts/2013-02-13-markdown-basics.md) лежит на гитхабе) можно тестировать в онлайн
редакторах:

* [http://stackoverflow.com/](http://stackoverflow.com/) — очень удобный редактор с превью и хоткеями
* [http://gist.github.com/](http://gist.github.com/) — выбрать формат `markdown`
* [http://markable.in/editor/](http://markable.in/editor/)

<h2 id="headings"><a href="#headings">
    Заголовки
</a></h2>

Заголовки обособляются хешами (хеш справа для красоты)

    ## Заголовки ##

От количества хешей зависит уровень заголовка:
    
    # Заголовок первого уровня (<h1/>) #
    ## Заголовок второго уровня (<h2/>) ##
    ### Заголовок третьего уровня (<h3/>) ###

**Главный заголовок** можно не выделять хешами, а подчеркнуть *двойной линией*:

    Погружение в маркдаун
    ================================================================================


**Второй по главности** заголовок можно не выделять хешами, а подчеркнуть *простой
линией*:

    Заголовки
    --------------------------------------------------------------------------------

<h2 id="text-formatting"><a href="#text-formatting">
    Форматирование текста
</a></h2>



### Абзацы и переносы ###

Новый абзац в маркдауне определяется по наличию *пустой строки* перед блоком
текста.  
Обычные одиночные переносы внутри маркдауна, допустим для поддержания длины
строки в 80 символов ни на что не влияют.

Для того, чтобы сделать перенос внутри строки, достаточно добавить два пробела
перед переносом строки.

Точки, это пробелы:  
[![markdown text editing](http://img22.imageshack.us/img22/9095/126a9dad309c445e95405c7.png)](http://img22.imageshack.us/img22/9095/126a9dad309c445e95405c7.png)


### Стилизация текста ###

* *Жирный текст** — `**Жирный текст**`
* *Курсивный текст* — `*Курсивный текст*`
* ***Жирный курсивный текст*** — `***Жирный курсивный текст***`

### Горизонтальная линия ###

--------------------------------------------------------------------------------

Горизонтальная линия в маркдауне до смешного проста

    --------------------------------------------------------------------------------

    Горизонтальная линия в маркдауне до смешного проста



<h2 id="links-n-images"><a href="#links-n-images">
    Вставка ссылок и картинок
</a></h2>


* [Ссылка на котиков](http://placekitten.com/) — `[Ссылка на котиков](http://placekitten.com/)`
* ![Описание картинки с котиком](http://placekitten.com/g/100/20) — `![Описание картинки с котиком](http://placekitten.com/g/100/20)`

**В большом тексте** удобно вставлять ссылки [сносками][1] как в книгах:

----
[1]: http://placekitten.com/ "Cat happens"

    **В большом тексте** удобно вставлять ссылки [сносками][1] как в книгах:

    ----
    [1]: http://placekitten.com/ "Cat happens"


<h2 id="lists"><a href="#lists">
    Списки
</a></h2>

### Обычный ненумерованный список ###

* один
* два

        * один
        * два

### Обычный нумерованный список ###

1. один
2. два

        1. один
        2. два

<h2 id="code"><a href="#code">
    Форматирование кода
</a></h2>

### Блочное форматирование кода ###

Для блочного выделения кода достаточно сделать отступ в 4 пробела или один таб.
Для такого представления:

    <ul class="nav">
        <li><a href="/atom.xml">RSS</a></li>
    </ul>

Нужно вставить в редактор такой код

        <ul class="nav">
            <li><a href="/atom.xml">RSS</a></li>
        </ul>    

### Строчное форматирование кода ###

Для строчного выделения `кода` достаточно обернуть в обратные кавычки:

    Для строчного выделения `кода` достаточно обернуть в обратные кавычки:

<h2 id="cite"><a href="#cite">
    Цитаты
</a></h2>

> Мы не поможем людям, делая за них то, что они могли бы сделать сами.

    > Мы не поможем людям, делая за них то, что они могли бы сделать сами.


<h2 id="html"><a href="#html">
    Обычный HTML
</a></h2>

Если что-то нельзя сделать в маркдауне, то используйте обычный HTML.
Допустим так:

    <h2 id="books"><a href="#books">
        Книги
    </a></h2>