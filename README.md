
This repository provides a comprehensive quick reference guide for various web development essentials, including responsive meta tags, favicons, CSS resets, and utility classes. It covers a range of topics such as:

- **Responsive Content Tag**: Ensuring optimal display on all devices.
- **Favicon**: Adding a recognizable icon to your website.
- **CSS Reset**: Standardizing default styles across browsers.
- **CSS Variables**: Using custom properties for maintainable and scalable styles.
- **Colors**: References to popular color palettes.
- **Fonts**: Importing and using web fonts effectively.
- **Font Icons**: Implementing scalable vector icons.
- **Media Queries**: Designing for different screen sizes.
- **Dark Mode**: Implementing a dark mode for your site.
- **Centered Content**: Centering elements with flexbox.
- **Cover Image**: Creating full-cover background images.
- **Cards**: Styling card elements with flat, neumorphic, and glassmorphic designs.
- **Flexbox and Grid Layouts**: Building responsive layouts with modern CSS techniques.
- **Shape Dividers and Filters**: Adding creative visual elements.
- **Animations**: Bringing your site to life with CSS animations.
- **Clipping Paths and Masks**: Creating complex shapes and visual effects.
- **Parallax Scrolling and Smooth Scrolling**: Enhancing user experience with scrolling effects.

This guide includes practical examples, references to generators and libraries, and links to further reading, making it a valuable resource for web developers looking to streamline their workflow.

<br>  

# Responsive Content Tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

# Favicon

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

# CSS Reset

```css
/* Reset CSS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

a { text-decoration: none; }
```

# CSS Variables
**Reference** https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties

```css
:root { --primary: #1e90ff; }
body { background-color: var(--primary); }
```

# Colors
**Reference** https://flatuicolors.com/, https://flatuicolors.com/palette/defo
**Generator** https://www.realtimecolors.com/?colors=e8f5ec-0b180f-a2d4b3-36316b-ae71be&fonts=Inter-Inter

# Fonts
**Source** https://fonts.google.com/

**Inspiration** https://fontjoy.com/, https://www.monotype.com/font-pairing#/playground

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');

body{ font-family:'Roboto'; }

/* 
rem: Relative to the root element
em: Relative to the parent element 

  <!-- 100vh will always represent the full height of the viewport, while 100% will depend on the height of the parent element. -->
  <!-- Grid provides control over both columns and rows, whereas Flexbox focuses on either the horizontal (main) axis or the vertical (cross) axis. Grid for layouts. Flexbox for groupings like icons, cards, etc. -->
*/
```

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
```

# Fonts Icons
**Source** https://ionic.io/ionicons 

```html
<script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
<script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
```

```html
<ion-icon name="heart"></ion-icon>
```

```css
ion-icon {font-size: 4rem;}
```

# Media Queries
```css
/* Design for Mobile First for faster mobile load times @media for larger screens */

/* and (orientation: landscape) */

/* Typical Device Breakpoints */ 
@media only screen and (max-width: 600px) {...}/* Extra small devices (phones, 600px and down) */
@media only screen and (min-width: 600px) {...}/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 768px) {...}/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 992px) {...}/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 1200px) {...}/* Extra large devices (laptops/desktops, 1200px and up) */
```

```html
<link rel="stylesheet" media="screen and (max-width: 600px)" href="smallscreen.css">
```

# Dark-Mode
**Reference** https://css-tricks.com/a-complete-guide-to-dark-mode-on-the-web/

```css
body {
  background-color: white;
  color: black;
}

.dark-mode {
  background-color: black;
  color: white;
}
```

```js
function myFunction() {
   var element = document.body;
   element.classList.toggle("dark-mode");
} 
```

# Centered Content

```css
.centerContentFlex { 
display: flex; 
justify-content: center; 
align-items: center; 
flex-wrap: wrap; 
}
```

# Cover Image
```css
.coverBG {background-image: url('bg.webp'); background-size: cover; background-position: center; }
```

```html
<div class="coverBG" style="height: 70vh;"> 
```

# Cards

```css
.flatCard{
    width:25vw;height:25vw; border-radius: 57px; background-color: dodgerblue ;color:#ffffff
}
```

# Nuemorphism
**Generator** https://neumorphism.io/#e0e0e0

```css
.neumorphicCard{
    width:25vw;height:25vw; border-radius: 57px;

    background: linear-gradient(145deg, #f1eaea, #cbc5c5);
    box-shadow:  19px 19px 37px #a9a4a4, -19px -19px 37px #ffffff;
}
```

# Glassmorphism
**Generator** https://hype4.academy/tools/glassmorphism-generator

```css
.glassmorphicCard{   
  width:25vw;height:25vw; border-radius: 57px;

  background: rgba( 255, 255, 255, 0.25 );
  box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
  backdrop-filter: blur( 4px );
  -webkit-backdrop-filter: blur( 4px );
  border-radius: 10px;
  border: 1px solid rgba( 255, 255, 255, 0.18 );
}
```

# Flex-Box
**Reference** https://css-tricks.com/snippets/css/a-guide-to-flexbox/

**Generator** https://www.cssportal.com/css-flexbox-generator/

```css
.flexContainer {
  display: flex; /* or inline-flex */
  flex-direction: row | row-reverse | column | column-reverse;
  flex-wrap: nowrap | wrap | wrap-reverse;
  flex-flow: column wrap;
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
  align-items: stretch | flex-start | flex-end | center | baseline;
  /* align-content only takes effect on multi-line flexible containers */
}
```

# Grid Layout
**Reference** https://css-tricks.com/snippets/css/complete-guide-grid/
**Generator** https://grid.layoutit.com/

```css
.gridContainer {
  display: grid;
  grid-template-columns: 50px 50px repeat(2,1fr);
  grid-template-rows: auto;
  grid-template-areas: 
  "header header header header"
  "main main . sidebar"
  "footer footer footer footer";

  column-gap: 10px; row-gap: 10px; /*optional*/
  justify-items: start | end | center | stretch;
  align-items: start | end | center | stretch;
}
```

```css
.item-a {grid-area: header;} .item-b {grid-area: main;} .item-c {grid-area: sidebar;} .item-d {grid-area: footer;}
```

```html
<div class="container">
<div class="item-a"></div>
<div class="item-b"></div>
<div class="item-c"></div>
<div class="item-d"></div>
</div>
```

# Shape Divider
**Generater** https://www.shapedivider.app/ - HTML must be copied into div with curves, and that div's position should be made relative.

# Filters
**Reference** https://www.w3schools.com/cssref/css3_pr_filter.php, https://www.w3schools.com/cssref/css3_pr_backdrop-filter.php

**Generator** https://cssgenerator.org/filter-css-generator.html, https://front-end-tools.com/en/generateBackDropFilter/

```css
filter/backdrop-filter: none | blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia() | url();

img {
  filter: blur(35px) drop-shadow(8px 8px 10px gray);
}
```

# Animations
**Reference** https://www.w3schools.com/css/css3_animations.asp

**Generator** https://webcode.tools/css-generator/keyframe-animation

**Library**   https://animate.style/, https://michalsnik.github.io/aos/ (Animate On Scroll Library), https://useanimations.com/ (Micro-animations)

# Clipping Paths and Masks
**Generator** https://bennettfeely.com/clippy/, https://www.google.com/search?q=Editing+PNG+Mask+Layer&udm=2

**Reference** https://www.w3schools.com/css/css3_masking.asp , https://www.w3schools.com/css/css3_masking.asp 

```css
clip-path: circle(50% at 50% 50%);
```

# Parallax Scrolling
**Reference**: https://www.w3schools.com/howto/howto_css_parallax.asp

```css
.parallax {
    background-image: url('path-to-image.jpg');
    min-height: 400px;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}
```

# Smooth Scrolling
For a scrolling box when scrolling is triggered by the navigation or CSSOM scrolling APIs.

```css
html {
    scroll-behavior: smooth;
}
```

# Additional
**Aspect-Ratio** https://www.w3schools.com/cssref/css_pr_aspect-ratio.php

**Parallex** https://www.w3schools.com/howto/howto_css_parallax.asp
**Shadows** https://cssgenerator.org/box-shadow-css-generator.html