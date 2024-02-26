# Noobslider

It's simple slider for photo. Nothing something else.

## Install

Write in console:

```
npm i noobslider
```

Import .css file and .js script in your HTML

```
<link rel="stylesheet" href="./node_modules/noobslider/style/style.css" />
<script src="./node_modules/noobslider/js/app.js"></script>
```

## Usage

Import script file to your js file

```
import Slider from "../node_modules/noobslider/js/app.js";
```

Make sure your HTML should be like this:

```
<div class="swiper">
      <div class="wrapper">
        <div class="photo slide">
        Your photo
        </div>
        <div class="photo slide">
        Your photo
        </div>
        <div class="photo slide">
        Your photo
        </div>
        <div class="photo slide">
        Your photo
        </div>
      </div>
    </div>
```

You can use any name of anything, but for slides you need add "slide" class.

Then init slide:

```
const main = document.querySelector(".swiper");

const wrapper = document.querySelector(".wrapper");

const slides = document.querySelector(".photo");

const res = new Slider(main, wrapper, slides, {
  indicator: {
    dots: true,
    number: false,
  },

  arrow: true,
});

res.initSlide();
```

## Customization

Slider has customization. Here settings:

```
new Slider(main, wrapper, slides, {
  indicator: {
    dots: true, // If you need dots indicator
    number: true, // If you need number of active slide
    border:true, // If you need border for dots indicator
    size: medium, // If you need change size of dots. Here 3 variants: medium, long, line
  },

  arrow: true, // If you need arrows for next or previous slide
});

```
