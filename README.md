# Logos inside of circles

## What is this?
logo-circles-svg is a repo of svg code that you can insert into your web page (if you want your visitor to see a circle with a logo inside of it)

## But why?
- I wanted [my website][(https://moist.biz)] to work like a business card of sorts, with links to my profiles elsewhere.
- Little circles take up less space than lots of words.
- Logos are easily recognizable on sight.

## What's inside these files?

Beginning of the Image:
```html
<!--- <a href="https://github.com/"> --->
<svg id="circle-svg-github-grey"
  width="35" height="35"
  viewBox="0 0 24 24"
  xmlns="http://www.w3.org/2000/svg"
  role="graphics-symbol img" 
  <title>GitHub</title>
```

> - The web address of the service is included as a comment.
> - `width=` and `height=` may be adjusted.
> - `viewBox=` needs values matching `0, 0, width, height` of the logo, plus a little for padding.

***

CSS Color Definitions:
```html
  <style type="text/css">
    .color-github-grey { fill: #24292d; }
    .color-white { fill: #ffffff; }
  </style>
```

***

The Circular Background:
```html
  <circle id="bg-github-grey"
    class="color-github-grey"
    cx="12" cy="12" r="12" />
```
> - The center points, `cx` and `cy`, are half of the width and height values defined above for the viewBox.
> - The radius of the circle, `r` = the larger of `cx` or `cy`.

***

The Logo:

