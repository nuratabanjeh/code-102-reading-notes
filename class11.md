## CSS Setting height and width for images :
**The height and width properties are used to set the height and width of an element.**
**The `height` and `width` properties do not include padding, borders, or margins. It sets the height/width of the area inside the padding, border, and margin of the element.**
```
img {
  height: 200px;
  width: 50%;
}
```
## How TO - Align Images Side By Side :
**Float Example :**
```
.column {
  float: left;
  width: 33.33%;
  padding: 5px;
}
.row::after {
  content: "";
  clear: both;
  display: table;
}
```
## Add Responsiveness :
**Optionally, you could add media queries to make the images stack on top of each other instead of floating next to each other, on a specific screen width.**
## CSS background-image :
**The `background-image` property specifies an image to use as the background of an element.**
**By default, the image is repeated so it covers the entire element.**
**Example:**
**The background image for a page can be set like this:**
```
body {
  background-image: url("paper.gif");
}
```
## CSS background-repeat Property :
**The `background-repeat` property sets if/how a background image will be repeated.**
**By default, a background-image is repeated both vertically and horizontally.**
**Tip: The background image is placed according to the background-position property. If no background-position is specified, the image is always placed at the element's top left corner.**
## CSS Linear Gradients :
**To create a linear gradient you must define at least two color stops. Color stops are the colors you want to render smooth transitions among. You can also set a starting point and a direction (or an angle) along with the gradient effect.**
```
Example
#grad {
  background-image: linear-gradient(red, yellow);
}
```
# What Is SEO?
**SEO stands for “search engine optimization.” It is the process of getting traffic from the “free,” “organic,” “editorial” or “natural” search results on search engines.**
## On-page SEO :
**On-page SEO is the practice of optimizing individual web pages in order to rank higher and earn more relevant traffic in search engines. On-page refers to both the content and HTML source code of a page that can be optimized, as opposed to off-page SEO which refers to links and other external signals.**
## HTML Audio and Video DOM Reference :
**The HTML5 DOM has methods, properties, and events for the `<audio>` and `<video>` elements.**
```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```
### The HTMLMediaElement API :
**Part of the HTML5 spec, the HTMLMediaElement API provides features to allow you to control video and audio players programmatically — for example HTMLMediaElement.play(), HTMLMediaElement.pause(), etc. This interface is available to both `<audio>` and `<video>` elements, as the features you'll want to implement are nearly identical. Let's go through an example, adding features as we go.**
## Getting started :
**To get started with this example, download our media-player-start.zip and unzip it into a new directory on your hard drive. If you downloaded our examples repo, you'll find it in javascript/apis/video-audio/start/**
**At this point, if you load the HTML you should see a perfectly normal HTML5 video player, with the native controls rendered.**
## Exploring the HTML :
**Open the HTML index file. You'll see a number of features; the HTML is dominated by the video player and its controls:**
```
<div class="player">
  <video controls>
    <source src="video/sintel-short.mp4" type="video/mp4">
    <source src="video/sintel-short.webm" type="video/webm">
    <!-- fallback content here -->
  </video>
  <div class="controls">
    <button class="play" data-icon="P" aria-label="play pause toggle"></button>
    <button class="stop" data-icon="S" aria-label="stop"></button>
    <div class="timer">
      <div></div>
      <span aria-label="timer">00:00</span>
    </div>
    <button class="rwd" data-icon="B" aria-label="rewind"></button>
    <button class="fwd" data-icon="F" aria-label="fast forward"></button>
  </div>
</div>
```
The whole player is wrapped in a `<div>` element, so it can all be styled as one unit if needed.
The `<video>` element contains two `<source>` elements so that different formats can be loaded depending on the browser viewing the site.
The controls HTML is probably the most interesting:
We have four `<button>`s — play/pause, stop, rewind, and fast forward.
Each `<button>` has a class name, a data-icon attribute for defining what icon should be shown on each button (we'll show how this works in the below section), and an aria-label attribute to provide an understandable description of each button, since we're not providing a human-readable label inside the tags. The contents of aria-label attributes are read out by screenreaders when their users focus on the elements that contain them.
There is also a timer `<div>`, which will report the elapsed time when the video is playing. Just for fun, we are providing two reporting mechanisms — a `<span>` containing the elapsed time in minutes and seconds, and an extra `<div>` that we will use to create a horizontal indicator bar that gets longer as the time elapses. To get an idea of what the finished product will look like, check out our finished version.
Exploring the CSS
Now open the CSS file and have a look inside. The CSS for the example is not too complicated, but we'll highlight the most interesting bits here. First of all, notice the .controls styling:
```
.controls {
  visibility: hidden;
  opacity: 0.5;
  width: 400px;
  border-radius: 10px;
  position: absolute;
  bottom: 20px;
  left: 50%;
  margin-left: -200px;
  background-color: black;
  box-shadow: 3px 3px 5px black;
  transition: 1s all;
  display: flex;
}
```
```
.player:hover .controls, player:focus .controls {
  opacity: 1;
}
```
**We start off with the visibility of the custom controls set to hidden. In our JavaScript later on, we will set the controls to visible, and remove the controls attribute from the `<video>` element. This is so that, if the JavaScript doesn't load for some reason, users can still use the video with the native controls.**
**We give the controls an opacity of 0.5 by default, so that they are less distracting when you are trying to watch the video. Only when you are hovering/focusing over the player do the controls appear at full opacity.**
**We lay out the buttons inside the control bar using Flexbox (display: flex), to make things easier.**
#### Next, let's look at our button icons:
```
@font-face {
   font-family: 'HeydingsControlsRegular';
   src: url('fonts/heydings_controls-webfont.eot');
   src: url('fonts/heydings_controls-webfont.eot?#iefix') format('embedded-opentype'),
        url('fonts/heydings_controls-webfont.woff') format('woff'),
        url('fonts/heydings_controls-webfont.ttf') format('truetype');
   font-weight: normal;
   font-style: normal;
}
```
```
button:before {
  font-family: HeydingsControlsRegular;
  font-size: 20px;
  position: relative;
  content: attr(data-icon);
  color: #aaa;
  text-shadow: 1px 1px 0px black;
}
```
### First of all, at the top of the CSS we use a @font-face block to import a custom web font. This is an icon font — all the characters of the alphabet equate to common icons you might want to use in an application.
**Next we use generated content to display an icon on each button:**
**We use the ::before selector to display the content before each `<button>` element.**
**We use the content property to set the content to be displayed in each case to be equal to the contents of the data-icon attribute. In the case of our play button, data-icon contains a capital "P".**
**We apply the custom web font to our buttons using font-family. In this font, "P" is actually a "play" icon, so therefore the play button has a "play" icon displayed on it.**
**Icon fonts are very cool for many reasons — cutting down on HTTP requests because you don't need to download those icons as image files, great scalability, and the fact that you can use text properties to style them — like color and text-shadow.**
**Last but not least, let's look at the CSS for the timer:**
```
.timer {
  line-height: 38px;
  font-size: 10px;
  font-family: monospace;
  text-shadow: 1px 1px 0px black;
  color: white;
  flex: 5;
  position: relative;
}
```
```
.timer div {
  position: absolute;
  background-color: rgba(255,255,255,0.2);
  left: 0;
  top: 0;
  width: 0;
  height: 38px;
  z-index: 2;
}
```
```
.timer span {
  position: absolute;
  z-index: 3;
  left: 19px;
}
```
We set the outer .timer `<div>` to have flex: 5, so it takes up most of the width of the controls bar. We also give it position: relative, so that we can position elements inside it conveniently according to it's boundaries, and not the boundaries of the `<body>` element.
The inner `<div>` is absolutely positioned to sit directly on top of the outer `<div>`. It is also given an initial width of 0, so you can't see it at all. As the video plays, the width will be increased via JavaScript as the video elapses.
The `<span>` is also absolutely positioned to sit near the left hand side of the timer bar.
We also give our inner `<div>` and `<span>` the right amount of z-index so that the timer will be displayed on top, and the inner `<div>` below that. This way, we make sure we can see all the information — one box is not obscuring another.





