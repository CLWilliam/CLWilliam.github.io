# Exploring CCS3 Improvements

As new features in CSS3 improve a more clean HTML structure
and introduces some new style controls without the need of extensive CSS framworks nor JS libraries,
I wanted to build a small project to try out basic front-end web development without bootstrap or MuiCSS.

## CSS Grid
My first feature to explore is the CSS grid system.
This system makes it very easy and understandable to divide the screen up in to different areas
and makes actual whitespace quite possible. No more endless structuring divs and 12 column systems.
The grid system makes it quite easy to switch designs for different layout, without running screaming towards bootstrap.

```css
#site {
    margin: 0px 0px 0px 0px;
    height: 100%;
    display: grid;
    grid-template-columns: 330px 8fr;
    grid-template-rows: 2fr 20fr 1fr;
    grid-template-areas:    "nav    title"
                            "nav    main"
                            "nav    footer";
}
```

## Smooth transitions
Smooth transitions were something I tried to implement with jquery when not going full-on bootstrap.
This one has been the easiest and the most compact solution to this problem. Where the overflow-y property is supported and part of CSS3,
the scroll-behaviour is still - at the time of writing - indicated as draft and not yet supported in Safari.
Not fully understanding the need for both properties (it doesn't work without overflow-y), I still need to dive into some docs to fully understand it.

```css
#site {
...
    scroll-behavior: smooth;
    overflow-y: scroll;
}
```
