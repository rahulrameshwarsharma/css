
*07 Jan 2024 Sunday morning 7am*
## Put the below code at the top of every css file
- **Below code will help to fix any default css already applied**
    * {
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
    border: border-box;
}

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
    Font-weight ranges between 100 - 900 (lighter, bold , bolder).

## box-model
    ** to make a circle give height and width equal value px, and border radius to 50%.

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

**align-items VS align-self**
- align-items applies on the container whereas align-self applies on individual items.
- align-self have higher priority then align-items.

## Media Queries
- Media queries make page responsive according to page size

- **keep color blue till 600px**
    - @media(max-width: 600px) {
                                    div {
                                        background-color: blue;
                                    }
                                }
-   **This above code turns the div into blue exactly before page width 600px.*

- **keep color red exactly at 600px**
    - @media(width: 600px) {
                                div {
                                    background-color: red;
                                } 
                            }
-   **This above code turns the div into red exactly at page width 600px.**

- **keep color blue after 600px**
    - @media(min-width: 600px) {
                                    div {
                                        background-color: blue;
                                    }
                                }

-   **This above code turns the div into blue exactly after page width 600px.*

**combine media queries together using "and" keyword**

@media (min-width: 200px) and (max-width: 400px) {
    div {
        background-color: orange;
    }
}

## Advance css
*Pseduo class*
- hover : it allows element to change it's css property when we take cursor on them.

- Active : it allows element to change it's css property when we click on them.

-    ## Transitions
    - transition-property: property that need transition (font-size, width etc.)
    - transition-duration: for how long that effect lasts (2s/4ms)
    - transition-timing-function: In how many steps that transition need to take place (ease-in/ease out/linear/steps).
    - transition-delay: after how much time the transition need to start (2s/4ms). And after how many second the transition need to restart after completion.

    - *All the transitions can apply in one line*
        - transition: propertyName|duration|timing-function|delay
        - transition: font-size 2s ease-in-out 0.2s;
        - if there not any specific property, then use "all" to apply in every property of that element.
        - transition: all 2s ease-in 1s;
- ## CSS Transform
    - used to apply 2D and 3D transformations to an element

- **Rotate**
    - *Rotate property is used to rotate element to a degree*

-    **this css transform degree property can be used to create a beautiful loarders manually**
    - Rotate property all types are
        - rotate: rotate:45deg; | rotateX: 45deg; | rotateY: 45deg; | rotateZ: 45deg;
    - This is the way to use "rotate" property in css code
        - transform: rotate(45deg);

- **Scale**
    - *Scale property is used to increase and decrease overall size of the element*
        - Scale property all types are
            - scale(2);| scale(0.5);| scale(1,2);| scaleX(0.5);| ScaleY(0.5);
        - This is the way to use "scale" property in code
            - transform: scale(2);
    
- **Translate**
    - *Translate property is used to move forward and backward complete element along the X & -X and Y & -Y axis.*

        - Translate property all types are
            - translate(20px);| translate(20px, 50px);| translateX(20px);| translateY(20px);
        - This is the way to use "translate" property in code
            - transform: translate(20px);

- **Skew**
    - *Skew property is used to stretch an element from both the corners*
        - This is the way to use "skew" property in code
            - transform: skew(45deg);

-   ## Animation
    - *To animate the element using css we use animation property*

        - For this, make an "animation keyframe" template first and then "write all properties"
        - "keyframes" are like blueprint for the animation.
        - To make template
            - @keyframe AnimationName {
                from {
                    font-size: 20px;
                }
                to {
                    font-size: 40px;
                }
            }
        - Instead of "from" and "to", "%" can also be used.
            - @keyframe AnimationName {
                0% {
                    font-size: 20px;
                }
                50% {
                    font-size: 30px;
                }
                100% {
                    font-size: 40px;
                }
            }

            - Basically "from" is "0%" and "to" is "100%".

        - Animation properties all the types are:
            - animation-name| animation-duration| animation-timing-function| animation-delay| animation-iteration-count(infinite,inherit,initial,5)| animation-direction(normal,reverse,alternate,alternate-reverse)|
        
        - This is the way to apply animation
            - div {
                Animation-name: colorAnimate;
                animation-duration: 3s;
                animation-timing-function: ease-in;
                animation-delay: 0s;
                animation-iteration-count: 5s;
                ani
            }
        - **Above code can also be written in one line**
        - *Animation property shorthand*
        - animation: animationName, duration, timing-function, delay, count, direction

            - div {
                animation: colorAnimate 2s ease-in 0s infinite normal;
            }
            @keyframes colorAnimate {
                from {
                    background-color: red;
                }
                to {
                    background-color: blue;
                }
            }