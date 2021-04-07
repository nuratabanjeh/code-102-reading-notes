# class05

## Images

### Adding Image

Images can be easily inserted at any section in an HTML page. To insert image in an HTML page, use the  tags. It is an empty tag, containing only attributes since the closing tag is not required.

`<img
  src="/html/images/test.png"
  alt="Simply Easy Learning"
  width="200"
  height="80"
/>`

### Aligning image

You can align image using align attribute

`<img src="images/bird.gif" alt="Bird" width="100" height="100" align="top" />`

You have four choices for alignment : top, bottom, left, right


Images with png formate is the best suit for screen displays.

Images with vsg format are vector based and it is the ultimate choice when using logo or icons in your website.

Images created for web should be saved at a resolution of 72ppi for optimization purpose.

### Figure and Figure caption

You can use `<figur>` tag to inclue a captions for the image element.

Example:

`<figure>`
 ` <img`
    `src="images/otters.jpg"
    alt="Photograph of
two sea otters floating in water"
  />`
  `<br />`
  `<figcaption>`
    Sea otters hold hands when they sleep so they don't drift away from each
    other.
  `</figcaption>`
`</figure>`

## CSS Color :
Color can really bring your pages to life :

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

 1. rgb values : These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)

 2. hex codes : These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80

 3. color names :There are 147 predefined color names that are recognized by browsers. For example: DarkCyan.




this information refrenced by :
 HTML & CSS Design and Build Websites By Jon Duckett 

CSS Fonts :
The CSS font properties define the font family, boldness, size, and the style of a text.

Difference Between Serif and Sans-serif Fonts:

![Difference Between Serif and Sans-serif Fonts](https://camo.githubusercontent.com/69c58a71256172df7057a77cc8f575af994f82c529fdca42e5f447fd57829831/68747470733a2f2f7777772e77337363686f6f6c732e636f6d2f6373732f73657269662e676966)

## CSS Units :

CSS has several different units for expressing a length.
Many CSS properties take "length" values, such as width, margin, padding, font-size, etc.Length is a number followed by a length unit, such as 10px, 2em, etc.A whitespace cannot appear between the number and the unit. However, if the value is 0, the unit can be omitted.For some CSS properties, negative lengths are allowed.There are two types of length units:
 absolute

 relative.

`|Unit |Description| |cm |centimeters| |mm |millimeters| |in |inches (1in = 96px = 2.54cm)| |px * |pixels (1px = 1/96th of 1in)| |pt |points (1pt = 1/72 of 1in)| |pc |picas (1pc = 12 pt)|`

**Thank you**
