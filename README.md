# Brad Bootcamp code and notes

Creator : LearnWebCode YT channel
Playlist link : https://www.youtube.com/playlist?list=PLpcSpRrAaOargYaCNYxZCiFIp9YTqEl-l

## 3. CSS Layout

0:00 Intro
**1:02 HTML - Starting**

- creates a header using a nav tag.
- add a logo
- add a ul with li and a children for menus
  **4:04 CSS - Starting**
- for nav li, use list style : none to remove bullet points
- set text color to white(#fff) and header bg color to custom blue
  **8:48 Flexbox**
- set header display to flex, and nav display to flex.
- use justify-content: space-between to align the logo and menu to the left and right respectively
- use align-items: center to align the logo and menu to the center
- use flex-wrap: wrap to wrap the menu to the next line if it doesn't fit in the header
- add margin-right to nav li for spacing between menu items
  **12:23 Attention to Details**
- add margin 0 to body tag. reseting default css
- adding padding 0 45px to header tag. `45px padding on the left and right`
- link a google font
- nav a:hover effect. to change color and transform rotate

```css
nav a:hover {
  color: #blue;
  transform: rotate(6deg);
}
```

- add display block to nav a to make rotate. `because rotate only works on block elements`
- add transition to nav a to make the rotate effect smooth
  - in nav a `transition: all 0.3s ease-in-out;`

20:40 Full Width BG Color / Inner Width Content

- Hero Section, div element to store headline, paragraph and link-button.
- in hero div class, add bgcolor as blue, padding 60px 45px.
- for big monitors, content is too wide, hard for reading.
- first try, set width as 600px but, extra white. add hero-inner div, set width as 760px, so now content is small.
- center horizontally, add display:flex and justify center to hero div.
- now if only width 760px, for **smaller mobiles**, content too wide, so instead use **max-width** 760px.
- style heading, paragraph(1.6rem, lh-1.6) and link(button class and style it.)

```css
.button {
  background-color: #3949ab;
  color: #fff;
  text-decoration: none;
  padding: 12px 20px;
  border-radius: 8px;
  font-size: 1.18rem;
  display: inline-block;
}
```

**36:30 CSS Grid**

- create html for grid, features.div>features-innerdiv.
- inside add div?featured-item div with h3,p. duplicate 9times.
- featured-inner > margin 0 auto, to center the section.
- use CSS grid to manage featured-items.

```css
.features-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  /* grid-template-columns: 300px 200px; */
  /* grid-template-columns: 33% 33% 33%; only 99%width not perfect.*/
  /* create horizontal scrollbar effect, cause padding adds to the width of 99% and exceeds viewport limit */
  /* so use 1fr 1fr 1fr, only uses available space after padding */
  /* grid-template-columns: repeat(4, 300px); */
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-column-gap: 45px;
  grid-row-gap: 45px;
}
```

## 4. Creating HTML Files(local setup, outside CodePen)

- basic stuff, uses figma to size images to a fixed size.
- use grid to layout images.

## 5. Free Hosting Github Pages

- uses create a Github a/c, use Github Desktop to push files to Github.
- using Github pages to host sites. Settings->Github Pages

## 6. Chrome Dev Tools and additonal Design skills

- Additonal things to learn about web design in free time.
  - Media queries
  - Flexbox
  - CSS Grid
  - Responsive images
- Chrome dev tools, inspect elements, check css styles.
- Deconstructing or reverse engineering Stripe background pattern.
- a card div with text, box-shadow
- div shape-one to create pattern in bg, using absolute positioning.

```css
.shape-one {
  positon: absolute;
  top: 100px;
  left: 0;
  right: 5%;
  background-color: #42a5f5;
  height: 80px;
  z-index: -1;
}
```

- create another shape-two div with similar style and diff color and top values.
- use transform: skewY(-10deg) to skew(rotate) the divs.
- apply trasnform to shapes div containing other shape.
- remember to add positon relative to parent of the shape section. so aboslute starts from there.
- overflow hidden to hide the skew effect bleeding into other sections.
- FIGMA basics
  - create gradients, copy css code and use in site.
  - SVG graphics for low size and retina display.
  - open svg file in text editor, copy code to html to use svg files instead of using svg files.
- Animate.css library for animations.

## 7. Bootstrap

- link to the Bootstrap cdn from docs.
  - `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">`

### Basic Classes

- styling link - <a class="btn btn-primary" ...>
  - has rounded corners, padding, blue color, no custom css code needed.
  - for larger button, btn-lg, or btn-small for small buttons.btn-outline-success, for bordered button
  - see bootstrap docs for button for diff buttons.

### Columns

- `container` class to auto center and set a wrapper
- div.row and two col divs inside it. both talk half space
- feature1, feature2, lorem ipsum descriptions
- using col-8 and col-4 for different widths.of two sectios.
- margin classes - in div row, add mt-4 for margin top, mx-4 and my-4.

### Responsive Classes

- col-md-6 for columns, md-medium screens.
- by default smallest, one column, not mentioned.
- col-lg-3, 4 columns, 12cols/3=4.
- find classnames from docs, Layout>Grid.

### Bootstrap JS

- not just buttons and clases
- **Bootstrap Components** - copy paste diff components, but it requires javascript. so import bootstrap js along with boostrap css. add link code at end of html code.

### Should you use bootsrap

- for larger projects, require custom mods
- for smaller, with little custom designs, can use bootstrap.
- use boostrap and not worry about css while learning other concepts like programming, backend, etc.
- hiring bootcamp grads, but can't implement custom designs not available in boostrap templates/components.
