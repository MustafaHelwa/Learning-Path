# CSS Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.  
**Project:** Learn CSS Colors by Building a Set of Colored Markers

---

## 1. Project Overview  

**Goal:** Create a simple webpage that showcases CSS color properties through a set of colored markers.  

---

## 2. HTML Structure  

- Start the `index.html` file with the `<!DOCTYPE html>` declaration, followed by the `<html lang="en">` tag, and conclude with the `</html>` closing tag.
- Add a `<head>` section to include metadata and a `<body>` section for the content.
  
### In the `<head>` section:
- **Title**: Define a title for SEO purposes using `<title>Colored Markers</title>`.
- **Charset**: Set character encoding to UTF-8 with `<meta charset="utf-8">`.
- **Viewport**: Make the page responsive with:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```
- **Stylesheet Link**: Connect the HTML file to `styles.css`:
  ```html
  <link rel="stylesheet" href="styles.css">
  ```

### In the `<body>` section:
- Add an `<h1>` tag for the heading content.
- Add a container `<div class="container"></div>` below the `<h1>` for the markers.

---

## 3. CSS Structure  

### Centering the Heading  
- Center the `<h1>` element:
  ```css
  h1 {
    text-align: center;
  }
  ```

### Marker Styling  
- Create a `.marker` class for each marker's size and positioning:
  ```css
  .marker {
    width: 200px;
    height: 25px;
    margin: 10px auto;
  }
  ```

- Add additional classes for individual marker colors:
  ```css
  .one {
    background-color: red;
  }
  
  .two {
    background-color: green;
  }
  
  .three {
    background-color: blue;
  }
  ```

### Applying Background and Padding  
- Set the container background to black using RGB:
  ```css
  .container {
    background-color: rgb(0, 0, 0);
  }
  ```

- Use shorthand padding for uniform top and bottom padding:
  ```css
  padding: 10px 0;
  ```

---

## 4. Color Models  

- **Hexadecimal Colors**: Example: `#00FF00` (0% red, 100% green, 0% blue) is the same as `rgb(0, 255, 0)`.
- **HSL (Hue, Saturation, Lightness)**: Example:
  ```css
  background-color: hsl(240, 100%, 50%);
  ```

- **Linear Gradient**: Example:
  ```css
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0));
  ```

---

## 5. Advanced Features  

### Adding Overlapping Elements  
- Add a `.sleeve` inside the red marker:
  ```html
  <div class="sleeve"></div>
  ```
- Set its style with opacity:
  ```css
  .sleeve {
    width: 110px;
    height: 25px;
    background-color: rgba(255, 255, 255, 0.5);
  }
  ```

### Display Inline Block  
- Use `display: inline-block;` to align two overlapping elements side by side.

---

## 6. Border and Shadow Styling  

### Border  
- Create a left border using:
  ```css
  border-left: 10px solid black;
  ```

### Box Shadow  
- Add shadows to make elements appear elevated:
  ```css
  box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);
  ```

---

## 7. Final Gradient and Shadow Combinations  

```css
.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);
}

.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 0 0 20px 0 #3B7E20CC;
}

.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 20px 0 hsla(223, 59%, 31%, 0.8);
}
```

---

## 8. Conclusion  

**Key Takeaways:**
- CSS offers multiple ways to define colors: RGB, Hex, HSL, and RGBA.
- Gradients and shadows enhance the visual appeal of elements.
- Shorthand properties like `padding` and `border` help simplify the code.


---
### Final Example Code `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colored Markers</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>CSS Color Markers</h1>
    <div class="container">
      <div class="marker red">
        <div class="cap"></div>
        <div class="sleeve"></div>
      </div>
      <div class="marker green">
        <div class="cap"></div>
        <div class="sleeve"></div>
      </div>
      <div class="marker blue">
        <div class="cap"></div>
        <div class="sleeve"></div>
      </div>
    </div>
  </body>
</html>
```

---

### Final Example Code `styles.css`:

```css
h1 {
  text-align: center;
}

.container {
  background-color: rgb(255, 255, 255);
  padding: 10px 0;
}

.marker {
  width: 200px;
  height: 25px;
  margin: 10px auto;
}

.cap {
  width: 60px;
  height: 25px;
}

.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left: 10px double rgba(0, 0, 0, 0.75);
}

.cap, .sleeve {
  display: inline-block;
}

.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);
}

.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 0 0 20px 0 #3B7E20CC;
}

.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 20px 0 hsla(223, 59%, 31%, 0.8);
}
```

---

### Output: 

![css preview](https://github.com/user-attachments/assets/c30ff911-f6e3-46ba-a084-a9f3607aad0c)

