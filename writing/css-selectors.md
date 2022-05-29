---
layout: layouts/article.njk
title: Css selectors
date: 2022-05-22T15:30
perex: In this article I am writing about basic css selectors
photo: css-selectors.jpg
alt: Types of css selectors
topics: html, css
timetoread: 5 minutes to read
tags: writing
---

Let´s have an example to practice these selectors. Create new html file named index.html and add following code to this file:

```
<!DOCTYPE html>
<html>
    <head>
        <title>css selectors</title>
        <style></style>
    </head>
    <body>
        <h1>Main Heading</h1>
         <h2>Heading1</h2>
                <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec fermentum, felis at sollicitudin sodales, nunc mauris sagittis eros, finibus lacinia nunc nunc quis ligula.</p>
          <h2>Heading2</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec fermentum, felis at sollicitudin sodales, nunc mauris sagittis eros, finibus lacinia nunc nunc quis ligula.</p>
    </body>
</html>
```

Now, let´s play with that selectors and text colors to see their precedence.
Between opening and closing `<style></style>` tags add:

```
* {
    color: gray;
  }
```

By this all text including headings change to gray color. That is universal selector.
Next I added **type** selectors:

```
h1 {
          color: blue;
        }
h2 {
          color: salmon;
        }
```

The result is changed color of h1 and h2, that means type selector overwrites the style of universal selector.

Now let´s look at **class** selector.
Add class to h1 heading.

```
<h1 class="mainclass">Main Heading</h1> and style it.
.mainclass {
    color: green;
    }
```

So class selector .mainclass overwrites the style of type and universal selector.

Some elements can contain class and **id** at the same time. By adding also id to Main header and styling it we´ll see that id style overwrites class style as below.
Let´s add id to h1: `<h1 id = "mainid" class="mainclass">Main Heading</h1>` and style it.

```
#mainid {
      color: pink;
    }
```

Complete code used in this example is:

```
<!DOCTYPE html>
<html>
<head>
    <title>css selectors</title>
    <style>
        * {
            color: gray;
        }
        h1 {
            color: blue;
        }
        h2 {
            color: salmon;
        }
        .mainclass {
            color: green;
        }
        #mainid {
            color: pink;
        }
    </style>
</head>

<body>
    <h1 id="mainid" class="mainclass">Main Heading</h1>
    <h2>Heading1</h2>
         <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec fermentum, felis at sollicitudin sodales, nunc mauris sagittis eros, finibus lacinia nunc nunc quis ligula.</p>
    <h2>Heading2</h2>
         <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec fermentum, felis at sollicitudin sodales, nunc mauris sagittis eros, finibus lacinia nunc nunc quis ligula.</p>
</body>
</html>
```

<div style="text-align: center;">
Thank you for stopping by and happy studying :)
</div>
