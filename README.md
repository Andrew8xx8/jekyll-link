Jekyll Link Plugin
===========

This is a [Jekyll plugin](https://github.com/mojombo/jekyll/wiki/Plugins) that generates 
links with additional classes if link href attribute is a part of a path of the current page.

This plugin will be very userful if you want to apply some additioinal styles to links 
that point out the current page.


Instalation
-----------

Place a `link.rb` file in your `plugins/` dir.

Usage
-----------

Plase this code in template:

```ruby
  {% link /contacts/ Contacts %}
```

It will be converted into this HTML on any page exepct contacts:

```html
  <a href="/contacts/">Contacts</a>
```

Extra class will be added in attributes on the contacts page:

```html
  <a href="/contacts/" class="current">Contacts</a>
```

Parent links will be marked with current class too.
For example we have to pages /about and subpage /about/author and template like this:

```html
 <ul>
   <li>
     {% link /about/ About %}
     <ul>
       <li>{% link /about/author Author %}
     </ul>
   </li>
 </ul>
```

On the /about/author all links will be generated as this:

```html
 <ul>
   <li>
     <a href="/about/" class="current">About</a>
     <ul>
       <li><a href="/about/author" class="current">Author</a>
     </ul>
   </li>
 </ul>
```
