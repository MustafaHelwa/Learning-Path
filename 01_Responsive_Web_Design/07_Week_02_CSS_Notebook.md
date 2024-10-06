# CSS Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.  
**Project:** Learn CSS Flexbox by Building a Photo Gallery

---

### HTML and CSS Step-by-Step Guide

#### Basic Setup

- **Starting with HTML basics:**
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Photo Gallery</title>
      <link rel="stylesheet" href="./styles.css">
    </head>
    <body>
    </body>
  </html>
  ```

- **Add a header to the body with an `<h1>`:**
  ```html
  <header class="header">
    <h1>CSS Flexbox Photo Gallery</h1>
  </header>
  ```

- **Add nine image elements inside a `<div>` with the class `gallery`:**
  ```html
  <div class="gallery">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg" alt="Sleep">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/2.jpg" alt="onBack">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/3.jpg" alt="gazee">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/4.jpg" alt="Sleep2">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/5.jpg" alt="cutie">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/6.jpg" alt="brothers">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/7.jpg" alt="whooah">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/8.jpg" alt="gheeee">
    <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/9.jpg" alt="blacknwhite">
  </div>
  ```

- **CSS for gallery and images:**
  - Adjust image styles with a uniform height and max width:
    ```css
    .gallery img {
      width: 100%;
      max-width: 350px;
      height: 300px;
    }
    ```

- **Remove body margin and set font and background:**
  ```css
  body {
    margin: 0;
    font-family: sans-serif;
    background-color: #f5f6f7;
  }
  ```

- **Style the header:**
  ```css
  .header {
    text-align: center;
    text-transform: uppercase;
    padding: 32px;
    background-color: #0a0a23;
    color: #fff;
    border-bottom: 4px solid #fdb347;
  }
  ```

- **Apply Flexbox layout to `.gallery`:**
  ```css
  .gallery {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 16px;
    max-width: 1400px;
    margin: 0 auto;
    padding: 20px 10px;
  }
  ```

- **Enhance image appearance with object-fit, border-radius, and gap:**
  ```css
  .gallery img {
    object-fit: cover;
    border-radius: 10px;
  }
  ```

- **Create an empty pseudo-element to maintain layout balance:**
  ```css
  .gallery::after {
    content: "";
    width: 350px;
  }
  ```

---

### Final HTML:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <link rel="stylesheet" href="./styles.css">
  </head>
  <body>
    <header class="header">
      <h1>css flexbox photo gallery</h1>
    </header>
    <div class="gallery">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/1.jpg" alt="Sleep">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/2.jpg" alt="onBack">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/3.jpg" alt="gazee">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/4.jpg" alt="Sleep2">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/5.jpg" alt="cutie">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/6.jpg" alt="brothers">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/7.jpg" alt="whooah">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/8.jpg" alt="gheeee">
      <img src="https://cdn.freecodecamp.org/curriculum/css-photo-gallery/9.jpg" alt="blacknwhite">
    </div>
  </body>
</html>
```

### Final CSS:

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: sans-serif;
  background: #f5f6f7;
}

.header {
  text-align: center;
  text-transform: uppercase;
  padding: 32px;
  background-color: #0a0a23;
  color: #fff;
  border-bottom: 4px solid #fdb347;
}

.gallery {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 16px;
  max-width: 1400px;
  margin: 0 auto;
  padding: 20px 10px;
}

.gallery img {
  width: 100%;
  max-width: 350px;
  height: 300px;
  object-fit: cover;
  border-radius: 10px;
}

.gallery::after {
  content: "";
  width: 350px;
}
```

---

**Final output**:

![Photo Gallery](https://github.com/user-attachments/assets/91a1e053-b0f0-4ea2-b6e2-0ab0c43f94a3)
