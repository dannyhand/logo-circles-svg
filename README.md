# Logos inside of circles

## What is this?

logo-circles-svg is a repo of svg code that you can insert into your web page (if you want your visitor to see a circle with a logo inside of it)

<img src="./svg/facebook-blue.svg"> <img src="./svg/linkedin-blue.svg"> <img src="./svg/snapchat-yellow-withstroke.svg"> <img src="./svg/instagram-pink.svg"> <img src="./svg/discord-purple.svg"> <img src="./svg/reddit-orange.svg"> <img src="./svg/github-grey.svg"> <img src="./svg/bluesky-blue.svg"> <img src="./svg/youtube-red.svg">

You can view all the current icons on one page in [icons.md](./icons.md)

## But why?

- Link to your social and gaming profiles from your website!
- Little circles take up less space than lots of words.
- Logos are easily recognizable on sight.
- It's a simple icon pack that a lot of work has gone into.

## What's inside these files?

Beginning of the Image:

```html
<!--- <a href="https://github.com/"> --->
<svg id="circle-svg-github-grey"
  width="35" height="35"
  viewBox="0 0 24 24"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
  role="link button img"
  preserveAspectRatio="xMidYMid meet">
  <title>GitHub</title>
```

> - The web address of the service is included as a comment.
> - `width=` and `height=` may be adjusted.
> - `viewBox=` needs values matching `0, 0, width, height` of the logo data.

##

CSS Color Definitions:
```html
  <style type="text/css">
    .color-github-grey { fill: #24292d; }
    .color-white { fill: #ffffff; }
  </style>
```

##

The Circular Background:
```html
  <circle id="bg-github-grey"
    class="color-github-grey"
    cx="12" cy="12" r="12" />
```
> - The center points, `cx` and `cy`, are half of the `width` and `height` values defined above for `viewBox=`.
> - The radius of the circle, `r` is the larger of `cx` or `cy`.

##

The Logo:  
If the group <g> element is used: 

```html
  <g id="logo-service-group-color"
    class="color-white"
    transform="scale(X,Y) translate(X,Y)">
    <path id="logo-service-piece1-color"
      d="PATHDATA" />
    <path id="logo-service-piece2-color"
      d="PATHDATA" />
  </g>
```

> - The `d=` field contains the math to draw a logo.
> - For the `id=` of a `<g>` or `<path>` element, the last part of the id is the `background color`. This allows to differentiate easily between separate id where only the background color is changed. ( i.e. `logo-reddit-orange` and `logo-reddit-blue` )
> - The optional `transform=` field (as well as the `class=` field) could be located inside the `<g>` element if it needs to be applied to each `<path>` element within. Otherwise it could be located inside an individual `<path>` element if only that particular `d=` needs to be affected.
>   - `scale(X,Y)` causes `d=` to shrink or grow. -- i.e. `scale(0.5,0.5)` would halve the size while maintaining the same aspect ratio.
>   - `translate(X,Y)` moves `d=` along the X and Y axis of the canvas defined by the `viewBox=` field.
> - Some logos use `<polygon>` or `<circle>` or other shapes in addition to `<path>`. Grouping, scale, and translate work the same way for these.

If the group <g> element is not used: 

```html
  <path id="logo-github-grey"
    class="color-white"
    transform="scale(0.685,0.685) translate(5.5,5.5)"
    d="M12,2C6.477,2,2,6.477,2,12c0,4.419,2.865,8.166,6.839,9.489c0.5,0.09,0.682-0.218,0.682-0.484c0-0.236-0.009-0.866-0.014-1.699c-2.782,0.602-3.369-1.34-3.369-1.34c-0.455-1.157-1.11-1.465-1.11-1.465c-0.909-0.62,0.069-0.608,0.069-0.608c1.004,0.071,1.532,1.03,1.532,1.03c0.891,1.529,2.341,1.089,2.91,0.833c0.091-0.647,0.349-1.086,0.635-1.337c-2.22-0.251-4.555-1.111-4.555-4.943c0-1.091,0.39-1.984,1.03-2.682C6.546,8.54,6.202,7.524,6.746,6.148c0,0,0.84-0.269,2.75,1.025C10.295,6.95,11.15,6.84,12,6.836c0.85,0.004,1.705,0.114,2.504,0.336c1.909-1.294,2.748-1.025,2.748-1.025c0.546,1.376,0.202,2.394,0.1,2.646c0.64,0.699,1.026,1.591,1.026,2.682c0,3.841-2.337,4.687-4.565,4.935c0.359,0.307,0.679,0.917,0.679,1.852c0,1.335-0.012,2.415-0.012,2.741c0,0.269,0.18,0.579,0.688,0.481C19.138,20.161,22,16.416,22,12C22,6.477,17.523,2,12,2z" />
</svg>
```

##

More to come, and please contribute more logos if you want.