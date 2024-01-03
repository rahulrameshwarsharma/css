
##  css changes priority defined by the order of tag in head tag
<head>
if styles tag is written first, then it will be excuted first and then external css, which gives output of external css
because in css, changes will be display as per the last executed code.
<style>
    body{
        color: blue;
    }
</style>
<link rel="stylesheet">

</head>

## css properties
    Font-weight ranges between 100 - 900 (lighter, bold , bolder)

## box-model
    ** to make a circle give height and width equal value px, and border radius to 50%

## Display properties
    ** block elements occupies 100% width (ex: div, h1).
    ** inline elements occupies width as per content in it (ex: span, button, input, a). also it don't allow to add margin & padding from top and bottom, only marging and padding from right and left will be applied by default.
    ** inline-block elements allow us to add margin and padding from all sides.
    ** display none property removes elements from the page, it doesn't reserves any space for the elements.
    ** visibility: hidden property reserves space for the element it just disappears form the place.

## units in css
    px is the absolute unit in css, where as %, em, rem, vh and vw are the relative units.
- %: it is used to give value according to parent and child relativity.
- em: it is relative to the font size of the parent, 2em means (2*font-size of the  parent).
- rem: (root em) it is relative to font size of text in root elements (like body or html).

## positions in css
- **positions**: static, absolute, relative, fixed, sticky, z-index.
    - static is the default, no other properties can be applied and have no effect.
    - relative makes element relative to itself. (position: fixed; right: 50px;) In this case element move 50px from its current position.
    - absolute uplift element from it's position relative to it's closest ancestor, and any nearby element automatically occupies it's place, as this uplifted, but at the same position.
    - fixed also uplifts element like absolute but it is positioned relative to browser.
    - sticky positioned based on scroll position.

## background image
- to use use "backgroung-image: url("img/image.jpg");
    - three size customization are available
        - cover, contain and [auto: defualt (contain)]
    - we usually use cover for better visibility.

## flexbox

