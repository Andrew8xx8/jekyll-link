Jekyll Link Plugin
===========

This is a [Jekyll plugin](https://github.com/mojombo/jekyll/wiki/Plugins) that generates 
links with additional classes if link href attribute is a part of a path of current page.

This plugin will be very userful if you want to apply some additioinal styles to links 
that point out the current page.


Instalation
-----------

Place a `link.rb` file in your `plugins/` dir.

Usage
-----------

Plase this code in template:

```
  {% link /contacts/ Contacts %}
```

It will be converted into this HTML on any page exepct contacts:

```
  <a href="/contacts/">Contacts</a>
```

On a contacts page in attributes will be added extra class:

```
  <a href="/contacts/" class="current">Contacts</a>
```
