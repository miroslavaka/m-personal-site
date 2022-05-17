![Image slider](/images/blog/image-slider.jpg)
In my self-study of programming, image slider becomes one of the first a bit more complex exercises I am trying to go through.
In this exercise I am going to use HTML, CSS and Javascript.

## My HTML:

Firts thing is to prepare basic html structure with links to css and js files:

```
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <script src="script.js"></script>
</body>
</html>
```

Save that file as index.html.

Next I insert images in html file and wrap them with `<div> `tag. I selected 4 images from the page: https://picsum.photos/. This page is great as you can select image and make it any width and height directly in link of image. For example image https://picsum.photos/id/29/800/500 is 800px wide and 500px height.

So let´s insert my selected images inside `<body>` tag:

```
<body>
   <div class="image-slider">
      <img src="https://picsum.photos/id/189/800/500" alt="">
      <img src="https://picsum.photos/id/196/800/500" alt="">
      <img src="https://picsum.photos/id/287/800/500" alt="">
      <img src="https://picsum.photos/id/29/800/500" alt="">
   </div>
  <script src="script.js "></script>
</body>
```

## CSS:

Following step is to style our image slide in CSS. To keep it simple I have just learnt from the internet resources to use only style which hides images:

```
  img {
        display: none;
    }

```

## Javascript:

Next steps lead us to Javascript where we unhide those images one by one. At beginning I would consider to use loop, but I have learnt again from online resources that for that case function setInterval() which is more appropriate. Inside setInterval() we set function to unhide images which will run every 3 seconds (3000 milliseconds):

```
  setInterval(function() {}, 3000);
```

But before next step I create array of images which we already have in html.

```
   let imgs = document.querySelectorAll('img');
```

I will loop though all images in that array therefore counter i is set to 0.

```
   let i = 0;
```

Up to now I have in our script.js file:

```
    let imgs = document.querySelectorAll('img');
    let i = 0;
    setInterval(function() {}, 3000);
```

Next I will unhide 1st image by adding style.display = 'block' to first image in array:

```
   let imgs = document.querySelectorAll('img');
    let i = 0;
    setInterval(function() {
        imgs[i].style.display = 'block';
    }, 3000);
```

As I did not increment i yet, is is still set to 0 which is the index of 1st image in array. After that 1st image will be visible in the browser.
Next increment i by one and all images are visible in the browser

```
   let imgs = document.querySelectorAll('img');
    let i = 0;
    setInterval(function() {
        imgs[i].style.display = 'block';
        i++;
    }, 3000);
```

But the thing is that we would like to make visible only one image in that array and all images remain invisible.

We will loop through array and ensure all images are hidden via style.display = 'none' and only one image with index i will be visible style.display = 'block'.

Now i is increasing infinitely because we do not set the upper boundary where it should stop. Upper boundary length of array. That we have to set by comparison if counter i is already the same value as array length then do not look for next image in that array but go to first image in the array and that is set i back to 0 index.

```
let imgs = document.querySelectorAll('img');
    let i = 0;
    setInterval(function() {
        imgs.forEach(img => {
            img.style.display = 'none';
        });
        if (i == imgs.length) {
            i = 0;
        }
        imgs[i].style.display = 'block';
        i++;
    }, 3000);
```

![Block of code](/images/blog/code-1.jpg)

<div style="text-align: center;">
Thank you for stopping by and happy studying :)
</div>
