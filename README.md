## [Natours](https://satyaki07.github.io/Natours/)
A responsive landing page for a travel agency startup. The site is built using HTML and CSS, making use of SASS preprocessor and following CSS BLOCK-ELEMENT-MODIFIER methodology.

## Features 
These are some of the key features of this landing page, showcasing different tricks and techniques avilable in CSS. 

---
### ```@keyframes``` animations
This feature allows for elements to transition from one position to another. This is achieved by defining where elements are positioned at the beginning and at the end of the animation (defined as 0% - 100%  - see below).
<p align="center">
    <img src="https://thumbs.gfycat.com/ElatedYawningDrongo-small.gif">
</p>

### Image Transitions
Each image is emphasized as it's hovered over giving a 3d-esque feel to the webpage. This is achieved by scaling-up the current image being hovered over and scale-down the other photos.

<p align="center">
    <img src="https://thumbs.gfycat.com/SoulfulAdvancedAtlasmoth-small.gif">
</p>

### Card Animations
Probably my most favorite feature of this page. This card animation is achieved by creating two div elements, front-side and back side, styled to be on top of each other achieved by the property ```backface-visibility: hidden``` and then giving each side it's own styling accordingly. This segment of this page also reuses the button component similar to the "Discover our tours" button at the top of the page.

<p align="center">
    <img src="https://thumbs.gfycat.com/TemptingPeskyLadybird-small.gif">
</p>

### Stories Section
This landing page also features a stories section where people review their experiences of the tours. The main highlights of this page is the background video (for this entire section), the container of the review being skewed into a parallelogram shape, and how the text *wraps* around the shape of the image.

<p align="center">
    <img src="https://thumbs.gfycat.com/ElderlyFlawedGrosbeak-size_restricted.gif">
</p>

<p align="center">
    <img src="https://thumbs.gfycat.com/GenerousImmaculateHoneybee-small.gif">
</p>

For the main content of this features section, we can see that the container is skewed into a parallelogram shape, and the text *wraps* around the image. The parallelogram shape of background of the container is achieved by skewing it by x degrees (in this case -12 degrees as seen below), and making sure that the rest of the contents inside of the container itself is skewed 12 degrees (opposite of its parent container).

Now the *wrapping around* of the text to the shape of the image is achieved by using CSS propert called, `shape-outside` and giving its specified values. Note however, that this will only work if the element has defined dimensions (width and height as seen on the code below).
Additionally, the image itself scales-down and blurs as this content section is hovered over. This can be achieved by using a CSS property called `filter` and a value of `blur` as seen in the code below.

## Responsive Design
This page also utilizes a responsive design to provide seamless user-experience to all users across all devices. This is achieved by utilizing a ```mixin``` where it takes in a breakpoint and with that, determins the max-width of the current viewport the app is being viewed from.

```css
@mixin respond($breakpoint) {
    @if $breakpoint == phone {
        @media (max-width: 37.5em) { @content }; // 600px
    }

    @if $breakpoint == tab-port {
        @media (max-width: 56.25em) { @content }; // 900px
    }

    @if $breakpoint == tab-land {
        @media (max-width: 75em) { @content }; // 1200px
    }

    @if $breakpoint == big-desktop {
        @media (min-width: 112.5em) { @content }; // 1800px
    }
}
```

## Technologies & Tools
+ HTML5
+ CSS3
+ npm
+ node-sass
+ live-server
