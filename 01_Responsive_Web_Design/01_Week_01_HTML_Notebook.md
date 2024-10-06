# HTML Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.

---
## Learn HTML by Building a Cat Photo App:

### Basic HTML Elements
- **Headline:**  
  `<h1>text</h1>`

- **Paragraph:**  
  `<p>text</p>`

- **Comment:**  
  `<!-- This is a comment -->`

- **Main Content Block:**  
  `<main>content</main>`

- **Image Tag:**  
  `<img src="URL" alt="description">`

- **Link to Another Page:**  
  `<a href="URL">Text</a>`  
  - Example:  
    `<p>See more <a href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>`

- **Open Link in New Tab:**  
  Add `target="_blank"` to the anchor tag.  
  - Example:  
    `<a href="URL" target="_blank">Text</a>`

- **Image Inside a Link:**  
  ```html
  <a href="example-link">
    <img src="image-link.jpg" alt="A photo of a cat.">
  </a>
  ```

### Structural Elements
- **Sectioning Content:**  
  `<section></section>`

- **Unordered List:**  
  `<ul></ul>`

- **Ordered List:**  
  `<ol></ol>`  
  - Example:  
    ```html
    <ol>
      <li>Flea treatment</li>
      <li>Thunder</li>
      <li>Other cats</li>
    </ol>
    ```

- **List Item:**  
  `<li>Item</li>`

- **Self-Contained Content:**  
  `<figure></figure>`

- **Figure Caption:**  
  `<figcaption>Caption text</figcaption>`

- **Emphasize Text:**  
  `<em>text</em>` (italicized)  
  - Example:  
    ```html
    <figure>
      <img src="lasagna.jpg" alt="Lasagna">
      <figcaption>Cats <em>love</em> lasagna.</figcaption>
    </figure>
    ```

- **Strong Text:**  
  `<strong>text</strong>` (bold)  
  - Example:  
    ```html
    Cats <strong>hate</strong> other cats.
    ```

### Forms and Inputs
- **Basic Form:**  
  `<form action="/submit-url"></form>`

- **Input Field (Text):**  
  `<input type="text" name="name">`  
  - Example:  
    ```html
    <input type="text" name="catphotourl" placeholder="cat photo URL">
    ```

- **Required Input Field:**  
  `<input required type="text" name="catphotourl">`

- **Button Element:**  
  `<button>Submit</button>`  
  - Alternative:  
    `<button type="submit">Submit</button>`

- **Radio Button:**  
  `<input type="radio">`

- **Checkbox:**  
  `<input type="checkbox">`

- **Grouping Input with Labels:**  
  ```html
  <label><input type="radio" name="option"> Label text</label>
  ```

- **Fieldset and Legend for Grouping:**  
  ```html
  <fieldset>
    <legend>Group title</legend>
    <!-- Inputs go here -->
  </fieldset>
  ```

### Document Structure and Metadata
- **HTML Declaration:**  
  `<!DOCTYPE html>`

- **Language Attribute for HTML:**  
  `<html lang="en">`

- **Head Section and Metadata:**  
  ```html
  <head>
    <meta charset="utf-8">
    <title>CatPhotoApp</title>
  </head>
  ```

- **Footer:**  
  ```html
  <footer>
    <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
  </footer>
  ```

---

### Final Example Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>CatPhotoApp</title>
</head>
<body>
  <main>
    <h1>CatPhotoApp</h1>

    <section>
      <h2>Cat Photos</h2>
      <p>See more <a href="https://freecatphotoapp.com" target="_blank">cat photos</a> in our gallery.</p>
      <a href="https://freecatphotoapp.com">
        <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">
      </a>
    </section>

    <section>
      <h2>Cat Lists</h2>
      <h3>Things cats love:</h3>
      <ul>
        <li>cat nip</li>
        <li>laser pointers</li>
        <li>lasagna</li>
      </ul>

      <h3>Top 3 things cats hate:</h3>
      <ol>
        <li>flea treatment</li>
        <li>thunder</li>
        <li>other cats</li>
      </ol>
    </section>

    <section>
      <h2>Cat Form</h2>
      <form action="https://freecatphotoapp.com/submit-cat-photo">
        <fieldset>
          <legend>Is your cat an indoor or outdoor cat?</legend>
          <label><input type="radio" name="indoor-outdoor" value="indoor" checked> Indoor</label>
          <label><input type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
        </fieldset>

        <fieldset>
          <legend>What's your cat's personality?</legend>
          <input type="checkbox" name="personality" value="loving" checked> <label for="loving">Loving</label>
          <input type="checkbox" name="personality" value="lazy"> <label for="lazy">Lazy</label>
          <input type="checkbox" name="personality" value="energetic"> <label for="energetic">Energetic</label>
        </fieldset>

        <input type="text" name="catphotourl" placeholder="cat photo URL" required>
        <button type="submit">Submit</button>
      </form>
    </section>
  </main>

  <footer>
    <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
  </footer>
</body>
</html>
```

---
