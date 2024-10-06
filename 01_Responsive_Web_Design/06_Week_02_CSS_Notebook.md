# CSS Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.  
**Project:** Learn the CSS Box Model by Building a [Rothko](https://en.wikipedia.org/wiki/Mark_Rothko) Painting

---

### HTML and CSS Step-by-Step Guide

#### Basic Setup
Start by creating a basic HTML structure for the project. This includes linking your CSS file and structuring your content.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Rothko Painting</title>
    <link href="./styles.css" rel="stylesheet">
  </head>
  <body>
  </body>
</html>
```

#### Adding the Canvas Structure
1. Replace any placeholder content with a `<div>` element that will act as the "canvas" of the painting.

```html
<div class="canvas"></div>
```

2. Add a frame around the canvas to style it as if it were an actual painting.

```html
<div class="frame">
  <div class="canvas"></div>
</div>
```

#### CSS Box Model: Styling the Elements
1. Define the size, background color, and other attributes of the canvas in the CSS file (`styles.css`).

```css
.canvas {
  width: 500px;
  height: 600px;
  background-color: #4d0f00;
  overflow: hidden;
  filter: blur(2px);
}
```

2. Style the frame to wrap around the canvas, adding a solid black border, padding, and centered margin.

```css
.frame {
  border: 50px solid black;
  width: 500px;
  padding: 50px;
  margin: 20px auto;
}
```

#### Adding Rectangles Inside the Canvas
1. Insert three `<div>` elements inside the canvas, each representing a different "rectangle" in the Rothko painting. These rectangles will have different colors, sizes, and positions.

```html
<div class="one"></div>
<div class="two"></div>
<div class="three"></div>
```

2. Style the first rectangle (class `one`).

```css
.one {
  width: 425px;
  height: 150px;
  background-color: #efb762;
  margin: 20px auto;
  box-shadow: 0 0 3px 3px #efb762;
  border-radius: 9px;
  transform: rotate(-0.6deg);
}
```

3. Style the second rectangle (class `two`).

```css
.two {
  width: 475px;
  height: 200px;
  background-color: #8f0401;
  margin: 0 auto 20px;
  box-shadow: 0 0 3px 3px #8f0401;
  border-radius: 8px 10px;
  transform: rotate(0.4deg);
}
```

4. Style the third rectangle (class `three`).

```css
.three {
  width: 91%;
  height: 28%;
  background-color: #b20403;
  margin: auto;
  filter: blur(2px);
  box-shadow: 0 0 5px 5px #b20403;
  border-radius: 30px 25px 60px 12px;
  transform: rotate(-0.2deg);
}
```

#### Applying Filters and Box Shadows
- Apply a blur filter to both `.one` and `.two` elements for a slight visual effect.

```css
.one, .two {
  filter: blur(1px);
}
```

- Box shadows and rounded corners (`border-radius`) are added to give depth and soften the edges of the rectangles.

### Final HTML Structure
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Rothko Painting</title>
    <link href="./styles.css" rel="stylesheet">
  </head>
  <body>
    <div class="frame">
      <div class="canvas">
        <div class="one"></div>
        <div class="two"></div>
        <div class="three"></div>
      </div>
    </div>
  </body>
</html>
```

### Final CSS Code
```css
.canvas {
  width: 500px;
  height: 600px;
  background-color: #4d0f00;
  overflow: hidden;
  filter: blur(2px);
}

.frame {
  border: 50px solid black;
  width: 500px;
  padding: 50px;
  margin: 20px auto;
}

.one {
  width: 425px;
  height: 150px;
  background-color: #efb762;
  margin: 20px auto;
  box-shadow: 0 0 3px 3px #efb762;
  border-radius: 9px;
  transform: rotate(-0.6deg);
}

.two {
  width: 475px;
  height: 200px;
  background-color: #8f0401;
  margin: 0 auto 20px;
  box-shadow: 0 0 3px 3px #8f0401;
  border-radius: 8px 10px;
  transform: rotate(0.4deg);
}

.one, .two {
  filter: blur(1px);
}

.three {
  width: 91%;
  height: 28%;
  background-color: #b20403;
  margin: auto;
  filter: blur(2px);
  box-shadow: 0 0 5px 5px #b20403;
  border-radius: 30px 25px 60px 12px;
transform: rotate(-0.2deg);
}
```

### Final Output

![Painting](https://github.com/user-attachments/assets/48773892-cad7-40cd-9e42-d4048984ada5)
