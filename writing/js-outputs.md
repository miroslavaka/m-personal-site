---
layout: layouts/article.njk
title: JS outputs
date: 2022-05-20T14:30
perex: In this article I am writing about basic js outputs.
photo: js-outputs.jpg
alt: JS outputs
topics: html, css, js
timetoread: 5 minutes to read
tags: writing
---

JavaScript handles output data in different ways. They are sent on screen using function or method:

- innerHTML - method
- document.write() - function
- window.alert() - function
- console.log() - method

To see how they exactly work, try this simple example:

```
<!DOCTYPE html>
<html>
<head>
     <meta charset="utf-8">
     <title>Output</title>
</head>
<html>
  <body>
     <p id="para">Paragraph</p>
     <script>
         var a, b;
         a = 5;
         b = 2;
        //innerHTML
        document.getElementById("para").innerHTML = a + b;
        //document.write
        document.write(a * b);
        //window.alert
        window.alert(a - b);
        //console.log
        console.log(a / b);
    </script>
  </body>
</html>
```

RESULTS are following:
innerHTML:
![Image1](/images/blog/code-2.jpg)

document.write():
![Image2](/images/blog/code-3.jpg)

window.alert():
![Image3](/images/blog/code-4.jpg)

console.log():
![Image4](/images/blog/code-5.jpg)

(find console.log() output under right click in browser and then - Inspect Element)

<div style="text-align: center;">
Thank you for stopping by and happy studying :)
</div>
