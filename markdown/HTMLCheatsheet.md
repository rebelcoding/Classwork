# HTML Cheatsheet

[Sample Code](https://github.com/cultureclap/username.github.io/tree/master)

Below we will run through a few basic HTML tags and examples.

We will run into most of these tags again as we scrape webpages.

As I said, when you know how to build something, you can unbuild; or in our case, navigate to what you want, and extract the data.

This notebook covers the following topics:

- Style tags
- Lists
- a tags
- Tables
- Div and Span


---
## HTML Foundation

```html
<html>
    <head>
        <title>Home</title>
    </head>
    <body>
        <h1>Welcome to SF</h1>
    </body>
</html>
```

---
## Style tags


<i>italics</i>
`<i>italics</i>`

<b>bold</b>
`<b>italics</b>`

<u>underline</u>
`<u>italics</u>`


---
## Images

`<img src="http://www.screamfreely.org/wp-content/uploads/2019/01/tahtGraf-e1548436884199.jpg"/>`
<img src="http://www.screamfreely.org/wp-content/uploads/2019/01/tahtGraf-e1548436884199.jpg"/>

`<img src="http://www.screamfreely.org/wp-content/uploads/2019/01/tahtGraf-e1548436884199.jpg" width="50%"/>`
<img src="http://www.screamfreely.org/wp-content/uploads/2019/01/tahtGraf-e1548436884199.jpg"  width="50%"/>

`<img src="http://www.screamfreely.org/wp-content/uploads/2019/01/tahtGraf-e1548436884199.jpg" width="25%"/>`
<img src="http://www.screamfreely.org/wp-content/uploads/2019/01/tahtGraf-e1548436884199.jpg"  width="25%"/>


---
## Lists

There are two types of lists, ordered and unordered.

### Unordered List

```html
<ul>
    <li>Item A</li>
    <li>Item B</li>
    <li>Item C</li>
    <li>Item D</li>
</ul>
```

<ul>
    <li>Item A</li>
    <li>Item B</li>
    <li>Item C</li>
    <li>Item D</li>
</ul>

### Ordered List

```html
<ol>
    <li>Item A</li>
    <li>Item B</li>
    <li>Item C</li>
    <li>Item D</li>
</ol>
```

<ol>
    <li>Item A</li>
    <li>Item B</li>
    <li>Item C</li>
    <li>Item D</li>
</ol>

---
## a href

The `a` tag links pages.

`<a href="https://www.duckduckgo.com">DuckDuckGo</a>`

Sometimes you may need to explicitly tell the browser to open the link in a new tab or window.

In this case you will use the `target` property of `<a>` tag.

`<a href="https://www.duckduckgo.com" target="_blank">DuckDuckGo</a>`

Other times you may want to link to a different part of the same page.

In order to do this you will use the `id` property, and provide an `id` wherever you wish to send the user, after they click on the link.

And then you provide a link using the `#` symbol.

```html
<a href="#Divs" target="_blank">DuckDuckGo</a>

<!-- somewhere further down the page -->

<h2 id="Divs">Div and Span</h2>

```

---
## Tables

A table is a basic structure in HTML, often used with or without borders, to format data.

Below is both a basic `table` structure, as well as a more complete example, with we will continue to examine.


```html
<table>
    <tr>
        <td>
            something
        </td>
    </tr>
</table>



<table>
    <tr>
        <td>
            <a href="https://www.duckduckgo.com">DuckDuckGo</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.ecosia.org/">Ecosia</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.hackthebox.eu/">Hack the Box</a>
        </td>
        <td>
            Online laboratory
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.youtube.com/watch?v=eXFGeZZbMzQ">Intro to Python Scripting in Maya</a>
        </td>
        <td>
            Video Tutorial
        </td>
    </tr>
</table>

```


<table>
    <tr>
        <td>
            <a href="https://www.duckduckgo.com">DuckDuckGo</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.ecosia.org/">Ecosia</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.hackthebox.eu/">Hack the Box</a>
        </td>
        <td>
            Online laboratory
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.youtube.com/watch?v=eXFGeZZbMzQ">Intro to Python Scripting in Maya</a>
        </td>
        <td>
            Video Tutorial
        </td>
    </tr>
</table>

Now let's add CSS to the mix, using the library [Bootstrap](https://getbootstrap.com/docs/3.3/getting-started/).

If you click on the link, you will be taken to a page with a subtopic entitled **Bootstrap CDN**.

Beneath this, will be a series of links; two theme options, and a JavaScript file.

We can use these scripts by importing them into our file, using the `<link>` tag.

Then, just by adding the `class` *table* we will see a significant change in how the `table` appears.


```html

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

<!-- For those interested in hacking, figure out what `sha384` means -->


<table class="table">
    <tr>
        <td>
            <a href="https://www.duckduckgo.com">DuckDuckGo</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.ecosia.org/">Ecosia</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.hackthebox.eu/">Hack the Box</a>
        </td>
        <td>
            Online laboratory
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.youtube.com/watch?v=eXFGeZZbMzQ">Intro to Python Scripting in Maya</a>
        </td>
        <td>
            Video Tutorial
        </td>
    </tr>
</table>

    
```






<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

<table class="table">
    <tr>
        <td>
            <a href="https://www.duckduckgo.com">DuckDuckGo</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.ecosia.org/">Ecosia</a>
        </td>
        <td>
            Search Engine
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.hackthebox.eu/">Hack the Box</a>
        </td>
        <td>
            Online laboratory
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.youtube.com/watch?v=eXFGeZZbMzQ">Intro to Python Scripting in Maya</a>
        </td>
        <td>
            Video Tutorial
        </td>
    </tr>
</table>


---
## Div and Span

Admittedly `<table>` tags can be difficult to use, especially if formatting a page for mobile users!

Many CSS libraries utilize the `class` property to create dynamic structures; and it is easiest to use them with `<div>` and `<span>` tags.

Neither tag does anything in particular, but is a placeholder denoting the existance of a grouping of *nested objects*.

```html

<div class="col-md-12">
    <div class="col-md-8">
        <a href="https://www.duckduckgo.com">DuckDuckGo</a>
    </div>
    <div class="col-md-4">
        Search Engine

    </div>
    <div class="col-md-8">
        <a href="https://www.ecosia.org/">Ecosia</a>
    </div>
    <div class="col-md-4">
        Search Engine

    </div>
    <div class="col-md-8">
        <a href="https://www.hackthebox.eu/">Hack the Box</a>
    </div>
    <div class="col-md-4">
        Online laboratory
    </div>
    <div class="col-md-8">
        <a href="https://www.youtube.com/watch?v=eXFGeZZbMzQ">Intro to Python Scripting in Maya</a>
    </div>
    <div class="col-md-4">
        Video Tutorial
    </div>

</div>

```



<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

<div class="col-md-12" style="padding: 5px 5px 25px 5px;">
    <div class="col-md-8">
        <a href="https://www.duckduckgo.com">DuckDuckGo</a>
    </div>
    <div class="col-md-4">
        Search Engine
    </div>
    <div class="col-md-8">
        <a href="https://www.ecosia.org/">Ecosia</a>
    </div>
    <div class="col-md-4">
        Search Engine
    </div>
    <div class="col-md-8">
        <a href="https://www.hackthebox.eu/">Hack the Box</a>
    </div>
    <div class="col-md-4">
        Online laboratory
    </div>
    <div class="col-md-8">
        <a href="https://www.youtube.com/watch?v=eXFGeZZbMzQ">Intro to Python Scripting in Maya</a>
    </div>
    <div class="col-md-4">
        Video Tutorial
    </div>
</div>

### Span

`<span>` tags are similar placeholders, but squishier.

It is used to inject specific code when necessary, but provides no changes by it self.

`<p>Here is a sentence in a <span style="color:green">paragraph</span> tag.</p>`

<p>Here is a sentence in a <span style="color:green">paragraph</span> tag.</p>