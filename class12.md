# The `<canvas>` element
**`<canvas>` element is similler to `<img>` element**
- `<canvas>` HTML element has two attributes (which are optional):
    1. `width`
       initial value if not specified : 300px
    2. `height`**
       initial value if not specified : 150px
- the `<canvas>` element can be styled with CSS like other images using the styling rules : `margin` , `border`, `background` , etc
- when no styling rules are applied to the `<canvas>` it will initially be fully transparent
### Fallback Content
**One difference between the `<img>` element and the `<canvas>` element is that with `canvas` you can define *fallback* content to displayed in browsers that don't support it**
- insert the alternate content inside the `<canvas>` element
- browsers that don't support `<canvas>` will ignore the container and render the fallback content inside it
- browsers that do support `<canvas>` will ignore the content inside the container, and just render the canvas normally.
**Another difference between `<canvas>` and `<img>`, and due to fallback content, a closing tag `</canvas>` is _required_ in `canvas`**
### The Rendering Context
- the `canvas` is initially blank
- the `<canvas>` element creates a fixed-size drawing surface that exposes one or more *_rendering contexts_*
- to display something, a script first needs to access the rendering context and draw on it
- the `getContext()` method is used by `canvas` to obtain the rendering context and its drawing functions
- `getContext()` takes one parameter which is the type of context
    - for 2d graphics : `'2d'` parameter
---------------------------------------------------------------
# Drawing shapes with canvas
## The Grid
**The grid is the _coordinate space_ of canvas**
- 1 unit in the grid corresponds to 1 pixel on the canvas
- all elements are placed relative to the origin
**`<canvas>` only supports two primitive shapes:**
1. rectangles
2. paths (lists of points connected by lines)
- other shapes must be created by combining one or more paths
### Drawing Rectangles
**There are three functions that draw rectangles on the canvas:**
1. **`fillRect(x, y, width, height)`**
    Draws a filled rectangle
2. **`strokeRect(x, y, width, height)`**
    Draws a rectangular outline
3. **`clearRect(x, y, width, height)`**
    Clears the specified rectangular area, making it fully transparent
- The parameters:
    - `x` and `y`
      specify the position on the canvas (relative to the origin)
    - `width` and `height`
      provide the rectangle's size
### Drawing Paths
**A path :   a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color**
**The function used to make shapes using paths:**
1. **`beginPath()`**
    Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up
2. **`closePath()`**
    Adds a straight line to the path, going to the start of the current sub-path
3. **`stroke()`**
    Draws the shape by stroking its outline
4. **`fill()`**
    Draws a solid shape by filling the path's content area
### Moving the pen
**`moveTo(x, y)` function is used to move the pen to the coordinates specified by `x` and `y`**
### Lines
**`lineTo(x, y)` function draws a line from the current drawing position to the position specified by `x` and `y`**

**Thankyou**