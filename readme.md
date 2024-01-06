
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
- There are 4 flexbox directions: row, row-reverse, column, column-reverse.
- there are two axis in flex property. ( Main axis and Cross axis)
    - row is the default direction i.e., from left to right.
    - row-reverse is from right to left. (flex-direction: row-reverse;)
    - column arranges all the elements vertically from (top to bottom).
    - column-reverse changes elements vertically from (bottom to top).

- ## flex properties used for flex containers
- total flex properties I learned are
- Justify-content, flex-wrap, align-items, align-content, align-self, flex-shrink, flex-grow.
    - justify-content: (flex-start, flex-end and center) => this three properties used to ship content at left, right and center without changing the direction of content.
        - space-around make equal space between elements but half of space in both the end of the element.
        - space-between makes equal space between all the elements but keeps no space in end of the element.
        - space-evenly makes equal space between all the elements including both the end of elements.
- **when we want all content in center**
    - give container "flex", keep flex-direction to "row" and justify-content to "center". It will align every item in center of box with no efforts.

- flex-wrap
    - Has 3 properties nowrap/wrap/wrap-reverse
    - used to wrap content inside the container.
    - **wrapping items creates space which can be solved by align-content**
- align-items: aligns items towards the cross-axis.
- align-content: alignment of space between and around the content
    - when we wrap content, empty space remains between the content, so **align content deals with that empty space**
- flex-shrink: allows to shrink item in any speed with respect to other items i.e., (flex-shrink: 1.5;).
- flex-grow: allows to grow item in any speed with respect to other items i.e., (flex-grow: 2.5;).


