Правила организации sprockets-ассетов в пекеджи
===============================================

В целях организации и структуризации sprockets-ассетов используется концепция пекеджей. Пекедж - сущность, которая
объединяет несколько javascript или css модулей в один файл. Правила объединения ассетов в пекеджи могут быть самыми
разными. Например:
- набор ассетов для конкретной страницы или набора страниц;
- набор ассетов по функциональности (модули для корзины, модуля для карточки товара и тд);
- набор ассетов для платформы (мобильная сборка, десктопная сборка);
- набор ассетов по происхождению (портальные, гемные, сторонние).

Пекеджи хранятся в следующих директориях:
- `app/assets/javascripts/package`
- `app/assets/stylesheets/package`

Пекеджи выполняют роль конфига, который указывает сборщику каким образом необходимо структурировать наши ассеты, поэтому
внутри пекеджа не должно быть никакого кода, а только инструкции подключения ассетов, весь код должен находится в
модулях.

Пример пекеджа с инструкциями подключения модулей:

```javascript
// = require jquery
// = require package/blog/auth
// = require blog/blog_settings
```