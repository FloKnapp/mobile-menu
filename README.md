# Animated mobile menu icon

This is a tiny css snippet for an animated mobile menu (hamburger) icon. 
It transitions from three bars to an 'X', indicating a close button.

Please take note that this repository only provides the icon and animation. 
For a fully functional menu feel free to take a look into the markup of 
the demo page, but this isn't the goal of this repository.

## Installation

Include the provided `mobile-menu.css` into your page and copy the following 
markup into your desired destination.

```html
<div class="mobile-menu-icon">
    <span class="line no1"></span>
    <span class="line no2"></span>
    <span class="line no3"></span>
</div>
```

To trigger the animation, add class `.open` to the container `.mobile-menu-icon`. 

Example:

| <img src="demo/closed.png" style="width: 70px" /> | ```<div class="mobile-menu-icon"></div>```<span style="padding-right: 2rem"></span> |
|---------------------------------------------------|-------------------------------------------------------------------------------------|
| <img src="demo/open.png" style="width: 70px" />   | ```<div class="mobile-menu-icon open"></div>```                                     |

## Change class on click

Use this snippet to toggle the class on click.

```html
// ...

<script>
(() => {
    document.addEventListener('DOMContentLoaded', () => {
        document
            .querySelector('.mobile-menu-icon')
            .addEventListener('click', () => {e.target.classList.toggle('open')});
    });
})();
</script>

```