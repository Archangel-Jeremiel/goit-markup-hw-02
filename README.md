# goit-markup-hw-02
/* 
Для того щоб ссилка була hover
після visited ставимо visited перед hover
.link {
    text-decoration: none;
    color: #212121;
}
.link:visited {
    color: #212121;
}
.link:hover,
.link:focus {
    color: #2196F3; */

/*
ПЕРЕМЕННАЯ
:root {
    --brand-color:#F5F5F5
}

ЦВЕТ текста
(1-всегда есть основной цвет; 
2-вторичный цвет текста;
3-как минимм один акцент.)

ХОВЕР,ФОКУС основа для ссылок(ФОКУС использется только на
интерактивных елементах(ссылки,кнопки)),(ХОВЕР может
использоватся визде)

.link:hover,
.link:focus {
    color: rgb(250, 0, 0, 10%);(90% цвета использется HEXADECIMAL
ХЕКС и в 10% RGB для прозрачности текста rgb(250, 0, 0, 10%)
} */

/* body {
    background-color: #FFFFFF;
    color:#757575;
} */

/* 
основной цвет текста - #757575;
вторичный цвет текста - #212121;
Хедер - #000000;
вторичный цвет текста - #FFFFFF; 
вторичный цвет текста - rgba(255, 255, 255, 0.6)
(#FFFFFF 60% для футера adress используем rgba);
акцент - #2196F3;
*/
/* Основные встроенные шрифты(которые ставятся дргим на случай если первый
не подключился):
- с засечками (sans)
- без засечек (sans-serif)
- моноширинные (monospace)
- курсивные (cursive)
- рукописные */

/* Базовые обозначения свойств шрифтов селектора:
-font-size (Задаёт размер шрифта элемента в абсолютных
или относительных единицах измерения.)
-font-weight (Контролирует толщину начертания 
(жирность, вес) букв шрифта.)
-font-style (Задаёт начертание текста, например можно
сделать текст наклонным (font-style: normal | italic |
oblique | initial | inherit).)
-font-family (Шрифт — это набор типографских литер,
цифр и специальных знаков определенного стиля для набора текста.) */

/* Базовые обозначения свойств шрифтов селектора:
-letter-spacing (Расстояния между буквами)
-word-spacing (Определяет интервал между словами.)
-text-decoration (Задаёт различное оформительное
-подчёркивание и другие эффекты текста.)
-text-transform (Управляет регистром символов в тексте,
например сделать все буквы заглавными или прописными.)
-text-align (Управляет выравниванием текстового содержимого 
элемента по горизонтали.)
-text-indent(Устанавливает величину отступа первой
строки блока текста, например абзаца.)
-line-height (Устанавливает межстрочный интервал 
(интерлиньяж, высоту строки) текста.)
-text-shadow (Контролирует тень текста, а также устанавливает
её параметры: цвет, смещение и радиус размытия.)
-white-space (По умолчанию браузер игнорирует больше одного 
пробела и переноса строки в HTML-разметке (normal | nowrap 
| pre | pre-wrap).) */

<!-- C помощю селектора "*" можно производить сброс этих значений до 0. Для этой цели подходит селектор с наименьшим приоритетом и одновременно такой, что задает правила для всех элементов.Приоритет у такого селектора минимальный (без ранга).
По умолчанию многие элементы (например заголовки) могут иметь значения `margin` отличные от `0`
По умолчанию у списка `padding-left` равен `40px` -->

<!-- Для тега li можно отменить свойство list-style с помощью значения none.
Селектор тега использовать нежелательно. Подходящим случаем для выбора тега в качестве селектора является необходимость отмены или обнуления стилей внутри документа. -->

<!-- В селектор можно ставить не только класс но и атрибут который должен быть в [] 
[type] {
    color:white;
}
button[type="reset"] {
    color:green;
} -->

<!-- Символ ^ для выбора тех значений атрибута, которые начинаются с определенных символов.
Нужен для выдиления однотипных елементов.
HTML
<a class="link" href="./index.html">На главную страницу</a>
<a class="link" href="#ancor">ссылка на элемент страницы с заданным id</a>
<section id="ancor">...</section>
В этом случае выделит все ссылки с символом #.
CSS
/* "#ancor" начинается с "#" */
[href^="#"] {
  color: red;

ещё пример
В этом случае выделит все ссылки с символом ./.
.link {
  text-decoration: none;
}
[href^="./"]
{
    color:red;
}
В этом случае выделит все ссылки с символом https.
[href^="https"] {
    color:navy;
}
} -->

<!-- Символ $ для выбора тех значений атрибута, которые заканчиваются на определенные символы.
Все тоже что и више только на конечные символы.
.link {
  text-decoration: none;
}
[href$="html"]{
    color:green;
}
[href$="css"]{
    color:orangered;
} -->

<!-- Тоже что и више но
Символ * для выбора тех значений атрибута, которые включают внутри в себя определенные символы
HTML
<ul>
  <li>
    <a class="link" href="./index.html">На главную</a>
  </li>
  <li>
    <a class="link" href="./about-book.html">О книге</a>
  </li>
  <li>
    <a class="link" href="./about-author.html">Об авторе</a>
  </li>
</ul>

<ul>
  <li>
    <a class="link" href="https://www.google.com/">Google</a>
  </li>
  <li>
    <a class="link" href="https://developer.mozilla.org/ru/docs/web/css">MDN + CSS</a>
  </li>
  <li>
    <a class="link" href="https://stackoverflow.com/questions/tagged/css">StackOverflow + CSS</a>
  </li>
</ul>
CSS
.link {
  text-decoration: none;
}
Будут выделены все атрибуты со словом about 
[href*="about"] {
    color:green;
}
Будут выделены все атрибуты со словом com 
[href*="com"] {
    color:orangered;
} -->

<!-- Атрибут ID имеет приоритет 2 ранга, он перекроет любое количество примененных класов 3 ранга(не желательно использовать в CSS используется в javaScript)
форма записи
HTML
<div class="warning" id="sending">Использование id в качестве селектора в большинстве случаев является плохой практикой. Потому что приводят к дублированию кода и, как следствие, к излишней сложности кода.</div>
CSS
#sending {
    background-color:teal;
    color:white;
}
} -->

<!-- Инлайн атрибут style имеет приоритет 1  ранга, он перекроет любое количество примененных ID 2 ранга
HTML
<div class="warning" id="inline" style="background-color:orange;
   color:navy">Инлайн стили нежелательно использовать из-за более высокого приоритета чем у id, а также из-за сложности c поддержкой и повторным использованием кода.</div>
   CSS
   .warning {
  background-color: white;
  color: red;
}
#inline {
  background-color: teal;
  color: white;
} -->

<!-- Значение !important добавляется после значения css свойства через пробел.
Использование этого способа изменить приоритет является плохим тоном и не рекомендуется к применению.
Пример записи в CSS
a {
  color: red !important;
}
Пример с инлайн стилем
<div style="color: navy !important;">Это css свойство невозможно ничем переопределить, т.к. сочетание инлайн и `!important` создают высший приоритет. Не используйте такой способ!</div>
-у тега приоритет 4-го ранга, после добавления !important ранг станет 04. Т.е. выше 1-го, 2-го, 3-го и 4-го рангов.
-у класса приоритет 3-го ранга, после добавления !important ранг станет 03. Т.е. выше 04-го, 1-го, 2-го, 3-го и 4-го рангов.
-у id приоритет 2-го ранга, после добавления !important ранг станет 02. Т.е. выше 03-го, 04-го, 1-го, 2-го, 3-го и 4-го рангов.
-у инлайн приоритет 1-го ранга, после добавления !important ранг станет 01. Т.е. выше 02-го, 03-го, 04-го, 1-го, 2-го, 3-го и 4-го рангов. -->

<!-- Отсчет соседства связан с потоком выполнения - т.е. началом отсчета соседства считается элемент, который написан и прочитан браузером первым. Первый сосед в селекторе задается с помощью символа +
Примеры с объяснением какой элемент является первым соседом.
HTML
<section class="first">
  Элемент
</section>
<section class="first-neighbor">
  1-й сосед
</section> 
<section class="second-neighbor">
  2-й сосед
</section> 
<section class="third-neighbor">
  3-й сосед
</section> 
CSS
.first + section {color: red;} -->

<!-- Отсчет соседства связан с потоком выполнения - т.е. соседними элементами считаются все элементы, написанные в коде после заданного селектором и имеющие общего прямого родителя. Любой нижний сосед для селектора задается с помощью символа ~
HTML
<section class="zero">сосед сверху</section>
<section class="first">Элемент</section>
<section class="first-neighbor">1-й сосед</section> 
<section class="second-neighbor">2-й сосед</section> 
<section class="third-neighbor">3-й сосед</section> 
CSS
.first ~ section {
  color: red;
} -->

<!-- Правильность подключения стилей
Т.к. правила CSS с равными селекторами, но записанными в тексте последними, перезапишут предыдущие значения для одинаковых свойств, то порядок подключения файлов CSS имеет значение.

Файл modern-normalize переопределяет некоторые стили браузера для удобства работы.
HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="css/modern-normalize.css" rel="stylesheet">
    <link href="css/style.css" rel="stylesheet">
</head>
<body>
</body>
</html> -->

<!-- ИЗУЧИТЬ
Отличие между свойством opacity и цветом прозрачности transparent:

opacity меняет прозрачность всех свойств элемента, связанных с цветом, а также прозрачность потомков элементов. Это ограничивает возможность применения свойства.

transparent это название цвета 'прозрачный', подобно названию белый - white или черный - black. Поэтому такое название можно применять для цвета текста, фона и т.п.

Пример наследования opacity -->

<!-- Задача 28/28
Чтобы получить удобство opacity в получении градаций прозрачности, но иметь возможность применять прозрачность только к определенному цвету используют альфа-канал. Это особый синтаксис для знакомой записи цвета в форматах rgb, hsl и hex.

В предыдущем примере мы выяснили, что недостаток transparency - отсутствие градаций, а недостаток opacity - неизбирательность (применятся ко всем цветам).

Чтобы избавиться от этих недостатков к форматам rgb, hsl и hex можно добавить 4-е значение - прозрачность или по другому - альфа-канал.

Синтаксис записи цвета с альфа-каналом:

rgba: rgba(Red,Green,Blue, Alfa), где значения Alfa меняется как у свойства opacity, т.е. от 0 до 1 с помощью дробных чисел. Например .5 - полупрозрачность.
hsla: hsla(Color, Saturation, Lightness, Alfa), где значения Alfa меняется как у свойства opacity, т.е. от 0 до 1 с помощью дробных чисел. Например .5 - полупрозрачность.
hexa: #RRGGBBAA), где AA - значения Alfa. Это меняется как у opacity , но в 16-ричном формате. Т.е. от 0 до FF. Например .5 = 80.
80-это середина в 16ричной системе -->