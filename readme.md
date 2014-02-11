## Imagine you need to create a website with 100.000 pages filled with user-generated content ##
- *How do you setup your frontend code?*
- *How do you ensure it’s compatible with all browsers you need to support?*

#### Answers ####

 - First off all we need to choose template engine for our site. It will help write all variants of interface

  - Templates may have structure like this: **"Main page"**, **"Inner page"**, **"Inner page without sidebar"**, **"Promo page for new product"**, **"Page for author's column"** и т.д.

  - Different controls from site have separate templates: **"News from Main Page"**, **"News from Inner page"**, **"Weather forecast"**, **"Quotes"** и т.д.
  
![Templates Example](http://d.snfr.us/Hk0p+)

 - I use "stylus" as a source for production-ready css, BEM css-naming. This approach allows me to keep styles for each block on page on a separate file. All code is visible on the first screen. It allows save more time on the work. I search files by the name in alphabetical order, it saves my time.

![Stylus example](http://kuznetsovanton.ru/projects/telegraaph/img/1st_example_1.jpg)

 - I use grunt for deploy and minification my code.
 - Manual testing and testing with BrowserStack.
 - I use graceful degradation for old browsers.
 - Separate styles for IE if it necessary.
 - Polyfills for new features that not supporting by old browsers like [html5shiv.js](https://github.com/aFarkas/html5shiv).
 - Basic file structure you can see on my [boilerplate](https://github.com/iSnifer/grunt-boilerplate) 


#### Ответы ####

 - Нужен шаблонизатор, который позволит строго описать все возможные варианты интерфейса.

  - Несколько оберточных шаблонов: **"Главная страница"**, **"Внутренняя страница"**, **"Внутренняя страница без бокового меню"**, **"Промо-страница нового продукта или колонки автора"** и т.д.

  - Выделить в отдельные файлы шаблоны компонентов, которые используются как на всем сайте, так и его отдельных шаблонах: **"Новости на главной"**, **"Новости на внутренних страницах"**, **"Прогноз погоды"**, **"Котировки"** и т.д.
  
![Templates Example](http://d.snfr.us/Hk0p+)

 - Для css я использую stylus, принятую БЭМ концепцию именования классов. Такой подход позволил хранить стили для каждого блока отдельно, размер css-кода убирается в рамках одного экрана, его легко поддерживать. Поиск по файлам в алфавитном порядке гораздо быстрее и удобнее, чем поиск в рамках большого css-файла на несколько сотен или тысяч строк.

![Stylus example](http://kuznetsovanton.ru/projects/telegraaph/img/1st_example_1.jpg)

 - За сборку и минификацию кода отвечает grunt.
 - Тестирование кода в различных браузерах производить как в ручную, так и с помощью BrowserStack.
 - Для старых версий браузеров, процент которых низок применить graceful degradation.
 - Там, где это необходимо - отдельные стили для IE.
 - Полифилы для новых фич, неподдерживаемых в старых браузерах, например, [html5shiv.js](https://github.com/aFarkas/html5shiv).
