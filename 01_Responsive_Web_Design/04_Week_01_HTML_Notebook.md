# HTML Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.  
**Project:** Learn HTML Forms by Building a Registration Form

---

## Starting with the HTML file:

### Setting up the basic structure:
- Define document type, language, and add head & body tags:
    ```html
    <!DOCTYPE html>
    <html lang="en">
      <head>
      </head>
      <body>
      </body>
    </html>
    ```

- Add the title and meta tag for character encoding:
    ```html
    <head>
      <meta charset="UTF-8">
      <title>Registration Form</title>
    </head>
    ```

- Link to the external CSS file:
    ```html
    <link rel="stylesheet" href="styles.css">
    ```

- Add a heading and paragraph within the body:
    ```html
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
    ```

### Creating a Form:
- Create a form that sends a response to the server:
    ```html
    <form action="https://register-demo.freecodecamp.org" method="post"></form>
    ```

- Add three fieldsets within the form to group elements logically:
    ```html
    <fieldset></fieldset>
    ```

- Add labels for First Name, Last Name, Email, and Password:
    ```html
    <label>Enter Your First Name:</label>
    <label>Enter Your Last Name:</label>
    <label>Enter Your Email:</label>
    <label>Create a New Password:</label>
    ```

- Apply `display: block;` to each label in CSS to place them on separate lines:
    ```css
    label {
      display: block;
      margin: 0.5rem 0;
    }
    ```

- Add input fields for each label:
    ```html
    <label>Enter Your First Name: <input id="first-name" type="text" required /></label>
    <label>Enter Your Last Name: <input id="last-name" type="text" required /></label>
    <label>Enter Your Email: <input id="email" type="email" required /></label>
    <label>Create a New Password: <input id="new-password" type="password" required minlength="8" /></label>
    ```

- Add a submit button at the end of the form:
    ```html
    <input type="submit" value="Submit" />
    ```

### Enhancements:
- Add a radio button group to choose account type (Personal or Business):
    ```html
    <fieldset>
      <legend>Account type (required)</legend>
      <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked /> Personal</label>
      <label for="business-account"><input id="business-account" type="radio" name="account-type" /> Business</label>
    </fieldset>
    ```

- Add a checkbox for terms and conditions:
    ```html
    <label for="terms-and-conditions">
      <input id="terms-and-conditions" type="checkbox" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
    </label>
    ```

- Add additional fields for uploading a profile picture, entering age, and selecting referral source:
    ```html
    <fieldset>
      <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" /></label>
      <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
      <label for="referrer">How did you hear about us?
        <select id="referrer">
          <option value="">(select one)</option>
          <option value="1">freeCodeCamp News</option>
          <option value="2">freeCodeCamp YouTube Channel</option>
          <option value="3">freeCodeCamp Forum</option>
          <option value="4">Other</option>
        </select>
      </label>
    </fieldset>
    ```

---

### CSS Styling:

- Set basic styles for the body, background, and text:
    ```css
    body {
      width: 100%;
      height: 100vh;
      margin: 0;
      background-color: #1b1b32;
      color: #f5f6f7;
      font-family: Tahoma;
      font-size: 16px;
    }
    ```

- Center the heading and paragraph:
    ```css
    h1, p {
      margin: 1em auto;
      text-align: center;
    }
    ```

- Style the form for better responsiveness:
    ```css
    form {
      width: 60vw;
      max-width: 500px;
      min-width: 300px;
      margin: 0 auto;
      padding-bottom: 2em;
    }
    ```

- Remove borders from fieldsets and apply padding:
    ```css
    fieldset {
      border: none;
      padding: 2rem 0;
      border-bottom: 3px solid #3b3b4f;
    }

    fieldset:last-of-type {
      border-bottom: none;
    }
    ```

- Style input fields and text areas:
    ```css
    input, textarea {
      background-color: #0a0a23;
      border: 1px solid #0a0a23;
      color: #ffffff;
      min-height: 2em;
    }
    ```

- Style the submit button:
    ```css
    input[type="submit"] {
      display: block;
      width: 60%;
      margin: 1em auto;
      height: 2em;
      font-size: 1.1rem;
      background-color: #3b3b4f;
      border-color: white;
    }
    ```

---

### Final HTML Code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Registration Form</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
    <form method="post" action='https://register-demo.freecodecamp.org'>
      <fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" name="first-name" type="text" required /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" name="last-name" type="text" required /></label>
        <label for="email">Enter Your Email: <input id="email" name="email" type="email" required /></label>
        <label for="new-password">Create a New Password: <input id="new-password" name="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>
      </fieldset>
      <fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input id="personal-account" type="radio" name="account-type" class="inline" checked /> Personal</label>
        <label for="business-account"><input id="business-account" type="radio" name="account-type" class="inline" /> Business</label>
      </fieldset>
      <fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" name="file" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" name="age" min="13" max="120" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer" name="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio" name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>
      </fieldset>
      <label for="terms-and-conditions">
        <input id="terms-and-conditions" type="checkbox" required name="terms-and-conditions" /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
      </label>
      <input type="submit" value="Submit" />
    </form>
  </body>
</html>
```

---

### Final CSS Code:

```css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
  font-family: Tahoma;
  font-size: 16px;
}

h1, p {
  margin: 1em auto;
  text-align: center;
}

form {
  width: 60vw;
  max-width:

 500px;
  min-width: 300px;
  margin: 0 auto;
  padding-bottom: 2em;
}

fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}

fieldset:last-of-type {
  border-bottom: none;
}

label, input[type="checkbox"] {
  display: block;
  margin: 0.5rem 0;
}

input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
  min-height: 2em;
}

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 1em auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
}
```

### Output: 

![css preview](https://github.com/user-attachments/assets/9b67f5d9-a4a2-4e6b-9d30-324d775ddc64)
