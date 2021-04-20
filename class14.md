# class14-a

# Transforms

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

`div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}`

## 2D Transforms

Two-dimensional transforms work on the x and y axes.

## 2D Rotate

The rotate value provides the ability to rotate an element from 0 to 360 degrees.

`<figure class="box-1">Box 1</figure>`

`<figure class="box-2">Box 2</figure>`

.box-1 {
  transform: rotate(20deg);
}

.box-2 {
  transform: rotate(-55deg);
}

## 2D Scale

Allows you to change the appeared size of an element.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`

 .box-1 {
  transform: scale(0.75);
}

.box-2 {
  transform: scale(1.25);
}

It is possible to scale only the height or width of an element using the scaleX and scaleY values.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`
`<figure class="box-3">Box 3</figure>`

.box-1 {
  transform: scaleX(0.5);
}

.box-2 {
  transform: scaleY(1.15);
}

.box-3 {
  transform: scale(0.5, 1.15);
}

## 2D Translate

The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`
`<figure class="box-3">Box 3</figure>`

.box-1 {
  transform: translateX(-10px);
}

.box-2 {
  transform: translateY(25%);
}

.box-3 {
  transform: translate(-10px, 25%);
}

## 2D Skew

skew, is used to distort elements on the horizontal axis, vertical axis, or both.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`
`<figure class="box-3">Box 3</figure>`

.box-1 {
  transform: skewX(5deg);
}

.box-2 {
  transform: skewY(-20deg);
}

.box-3 {
  transform: skew(5deg, -20deg);
}

## Combining Transforms

It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`

.box-1 {
  transform: rotate(25deg) scale(0.75);
}

.box-2 {
  transform: skew(10deg, 20deg) translateX(20px);
}

## Transform Origin

As previously mentioned, the default transform origin is the dead center of an element, both 50% horizontally and 50% vertically. To change this default origin position the transform-origin property may be used.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`
`<figure class="box-3">Box 3</figure>`
`<figure class="box-4">Box 3</figure>`

.box-1 {
  transform: rotate(15deg);
  transform-origin: 0 0;
}

.box-2 {
  transform: scale(0.5);
  transform-origin: 100% 100%;
}

.box-3 {
  transform: skewX(20deg);
  transform-origin: top left;
}

.box-4 {
  transform: scale(0.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}

## Perspective

In order for three-dimensional transforms to work the elements need a perspective from which to transform.

`<figure class="box">Box 1</figure>`
`<figure class="box">Box 2</figure>`
`<figure class="box">Box 3</figure>`

.box {
  transform: perspective(200px) rotateX(45deg);
}

## Perspective Depth Value

The perspective value can be set as none or a length measurement.

3D Rotate

With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`
`<figure class="box-3">Box 3</figure>`

.box-1 {
  transform: perspective(200px) rotateX(45deg);
}

.box-2 {
  transform: perspective(200px) rotateY(45deg);
}

.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}

## 3D Scale

By using the scaleZ three-dimensional transform elements may be scaled on the z axis.

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`

.box-1 {
  transform: perspective(200px) scaleZ(1.75) rotateX(45deg);
}

.box-2 {
  transform: perspective(200px) scaleZ(0.25) rotateX(45deg);
}

## 3D Translate

Elements may also be translated on the z axis using the translateZ value.


.box-1 {
  transform: perspective(200px) translateZ(-50px);
}
.box-2 {
  transform: perspective(200px) translateZ(50px);
}

## 3D Skew

Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale.

## Transform Style

To allow nested elements to transform in their own three-dimensional plane use the transform-style property with the preserve-3d value.

`<div class="rotate three-d">`
  `<figure class="box">Box 1</figure>`
`</div>`
`<div class="rotate">`
  `<figure class="box">Box 2</figure>`
`</div>`

.rotate {
  transform: perspective(200px) rotateY(45deg);
}

.three-d {
  transform-style: preserve-3d;
}

.box {
  transform: rotateX(15deg) translateZ(20px);
  transform-origin: 0 0;
}

## Transitions & Animations

## Transitions

* CSS transitions allows you to change property values smoothly, over a given duration.

* There are two properties that are required in order for the transition to take effect:

1. transition-property

2. transition-duration

3. Transition Shorthand

div {
  transition: [property] [duration] [timing-function] [delay];
}

## transition-property

The transition-property specifies the CSS property where the transition will be applied. You may apply a transition to an individual property (e.g., background-color or tranform) or to all properties in the rule-set (i.e., all).

CSS syntax examples for transition-property

div {
  transition-property: all;
  transition-property: transform;
}

## transition-duration

The transition-duration property specifies the time span of the transition. You can specify in seconds or milliseconds.

CSS syntax example for transition-duration

div {
  transition-duration: 3s;
}
Shorthand example for transition-duration

div {
  transition: all 3s;
}

## transition-timing

The transition-timing-function property allows you to define the speed of the transition over the duration. The default timing is ease, which starts out slow, quickly speeds up, and then slows down at the end. The other timing options are: linear, ease, ease-in, ease-out, and ease-in-out.

div {
  transition: all 3s 1s;
}

## Animation

* An animation lets an element gradually change from one style to another.

* You can change as many CSS properties you want, as many times you want.

* To use CSS animation, you must first specify some keyframes for the animation.

* Keyframes hold what styles the element will have at certain times.

## The @keyframes Rule

When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.

@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}

## Delay an Animation

The animation-delay property specifies a delay for the start of an animation.

The following example has a 2 seconds delay before starting the animation:

Example:

div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
}

## Run Animation in Reverse Direction or Alternate Cycles

The animation-direction property specifies whether an animation should be played forwards, backwards or in alternate cycles.

The animation-direction property can have the following values:

* normal - The animation is played as normal (forwards). This is default

* reverse - The animation is played in reverse direction (backwards)

* alternate - The animation is played forwards first, then backwards

* alternate-reverse - The animation is played backwards first, then forwards

div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}

## Specify the Speed Curve of the Animation

The animation-timing-function property specifies the speed curve of the animation.

The animation-timing-function property can have the following values:

* ease - Specifies an animation with a slow start, then fast, then end slowly (this is default)

* linear - Specifies an animation with the same speed from start to end

* ease-in - Specifies an animation with a slow start

* ease-out - Specifies an animation with a slow end

* ease-in-out - Specifies an animation with a slow start and end

* cubic-bezier(n,n,n,n) - Lets you define your own values in a cubic-bezier function

**Thank you**