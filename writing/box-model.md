---
layout: layouts/article.njk
title: Box model
date: 2022-06-01T19:30
perex: I try visually explain difference between "box-sizing:content-box" and "box-sizing:border-box"
photo: box-model1.jpg
alt: Box model
topics: html, css
timetoread: 2 minutes to read
tags: writing
---

While studying css basics, it took me some examples to caught how box-sizing incorporated within css influences overall width and height of the element.

Here I try visually explain difference between **box-sizing:content-box** and **box-sizing:border-box**.

Actual width of element is calculated = width + padding + margin
Actual height of element is calculated = height + padding + margin

**BOX-SIZING: CONTENT-BOX**

in this case content does not include padding and margin so padding and margin increase actual width and height of the element
![Block of code](/images/blog/box-model2.jpg)

**BOX-SIZING: BORDER-BOX**

in this case content will include padding and margin so padding and margin do not increase actual width and height of the element
![Block of code](/images/blog/box-model3.jpg)

<div style="text-align: center;">
Thank you for stopping by and happy studying :)
</div>
