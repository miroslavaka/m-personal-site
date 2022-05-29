---
layout: layouts/article.njk
title: R1C1 formula
date: 2022-05-22T14:00
perex: In this article I am writing about construction of r1c1 formula in excel format
photo: excel-5.jpg
alt: r1c1 formula
topics: vb
timetoread: 5 minutes to read
tags: writing
---

Formulas in excel are very powerful and the style how excel write formulas is so called A1 style. But macro recorder uses formula R1C1 (R[1]C[1]) style.

![Excel5](/images/blog/excel-5.jpg)

R1C1 style
cell C14 references cell A14 (row 14, column 1) and cell B14 (row14, column2). This is an absolute reference ($ symbol in front of the row number and column letter). Range("C14").FormulaR1C1 = "=R14C1\*R14C2".

![Excel6](/images/blog/excel-6.jpg)

![Excel7](/images/blog/excel-7.jpg)

R[1]C[1] style
cell C20 references cell A20 (the same row and two columns to the left) and cell B20 (the same row and one column to the left). This is a relative reference. Range("C20").FormulaR1C1 = "=RC[-2]\*RC[-1]".

![Excel8](/images/blog/excel-8.jpg)

Explanation of R1C1 formula style:
For example R[1]C[2] is a cell 1 row down and 2 columns to the right.
R[-1]C[-2] is a cell 1 row up and 2 columns to the left.
If no number is shown in brackets then you are referring to the same row or column i.e. R[1]C will be a 1 row below the current cell in the same column.

![Excel9](/images/blog/excel-9.jpg)

<div style="text-align: center;">
Thank you for stopping by and happy studying :)
</div>
