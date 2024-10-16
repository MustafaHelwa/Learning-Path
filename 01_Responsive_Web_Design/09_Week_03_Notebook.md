### HTML and CSS Learning Journey Notebook

**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.  
**Project:** Learn Accessibility by Building a Quiz

---

### HTML and CSS Step-by-Step Guide

#### Basic Setup

1. **Starting with Basic HTML and CSS Code:**

   **HTML:**
   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
       <title>Accessibility Quiz</title>
       <link rel="stylesheet" href="styles.css" />
     </head>
     <body>
       <header>
           <img id="logo" src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" alt="freeCodeCamp">
           <h1> HTML/CSS Quiz</h1>
           <nav></nav>
       </header>
       <main></main>
     </body>
   </html>
   ```

   **CSS:**
   ```css
   body {
     background: #f5f6f7;
     color: #1b1b32;
     font-family: Helvetica;
     margin: 0;
   }
   ```

2. **Set a Maximum Width for the Logo:**

   ```css
   #logo {
     width: max(10rem, 18vw);
     background-color: #0a0a23;
     aspect-ratio: 35 / 4;
     padding: 0.4rem;
   }
   ```

3. **Style the Header:**

   ```css
   header {
     width: 100%;
     height: 50px;
     background-color: #1b1b32;
     display: flex;
   }
   ```

4. **Adjust the Heading Font Size and Color:**

   ```css
   h1 {
     color: #f1be32;
     font-size: min(5vw, 1.2em);
   }
   ```

5. **Create a Navigation List:**

   ```html
   <nav>
     <ul>
       <li><a>INFO</a></li>
       <li><a>HTML</a></li>
       <li><a>CSS</a></li>
     </ul>
   </nav>
   ```

6. **Style the Navigation List Using Child Combinator Selector:**

   ```css
   nav > ul {
     justify-content: space-evenly;
     display: flex;
   }
   ```

7. **Add a Form with Sections in the Main Element:**

   ```html
   <main>
     <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
       <section></section>
       <section></section>
       <section></section>
     </form>
   </main>
   ```

8. **Define Roles for Sections:**

   ```html
   <section role="region"></section>
   <section role="region"></section>
   <section role="region"></section>
   ```

9. **Add Aria-Labelledby Attributes to Sections:**

   ```html
   <section role="region" aria-labelledby="student-info">
     <h2 id="student-info">Student Info</h2>
   </section>
   <section role="region" aria-labelledby="html-questions">
     <h2 id="html-questions">HTML</h2>
   </section>
   <section role="region" aria-labelledby="css-questions">
     <h2 id="css-questions">CSS</h2>
   </section>
   ```

10. **Style Headings and Add Borders to H2 Elements:**

    ```css
    h1, h2 {
      font-family: Verdana, Tahoma;
    }
    h2 {
      border-bottom: 4px solid #dfdfe2;
    }
    ```

11. **Link Navigation Anchors to Section IDs:**

    ```html
    <ul>
      <li><a href="#student-info">INFO</a></li>
      <li><a href="#html-questions">HTML</a></li>
      <li><a href="#css-questions">CSS</a></li>
    </ul>
    ```

12. **Add Input and Label Elements Inside the Student Info Section:**

    ```html
    <section role="region" aria-labelledby="student-info">
      <h2 id="student-info">Student Info</h2>
      <div class="info">
        <label for="student-name">Name:</label>
        <input type="text" name="student-name" id="student-name" />
      </div>
      <div class="info">
        <label for="student-email">Email:</label>
        <input type="email" name="student-email" id="student-email" />
      </div>
      <div class="info">
        <label for="birth-date">Date of Birth:</label>
        <input type="date" name="birth-date" id="birth-date" />
      </div>
    </section>
    ```

13. **Add Placeholder for Name Input:**

    ```html
    <input type="text" name="student-name" id="student-name" placeholder="e.g. Omar Ali" />
    ```

14. **Add Questions in the HTML Section with Radio Inputs:**

    ```html
    <section role="region" aria-labelledby="html-questions">
      <h2 id="html-questions">HTML</h2>
      <div class="question-block">
        <h3>1</h3>
        <fieldset class="question">
          <legend>Is this statement true?</legend>
          <ul class="answers-list">
            <li>
              <label for="q1-a1">
                <input type="radio" id="q1-a1" value="True" name="q1a"/> True
              </label>
            </li>
            <li>
              <label for="q1-a2">
                <input type="radio" id="q1-a2" value="False" name="q1a"/> False
              </label>
            </li>
          </ul>
        </fieldset>
      </div>
    </section>
    ```

15. **Ensure Radio Inputs Use the Same Name Attribute for Each Question:**

    ```html
    <input type="radio" id="q1-a1" value="true" name="q1a" />
    ```

16. **Use a Before Pseudo-Element to Add Content Before H3:**

    ```css
    h3::before {
      content: "Question #";
    }
    ```

17. **Add Select Dropdown in the CSS Section:**

    ```html
    <section role="region" aria-labelledby="css-questions">
      <h2 id="css-questions">CSS</h2>
      <div class="question-block">
        <label for="selector">Can the CSS margin property accept negative values?</label>
        <select name="selector" id="selector" required>
          <option value="">Select an option</option>
          <option value="yes">Yes</option>
          <option value="no">No</option>
        </select>
      </div>
    </section>
    ```

18. **Add a Textarea for Additional Questions:**

    ```html
    <div class="question-block">
      <label for="textbox">Do you have any questions:</label>
      <textarea rows="5" cols="24" id="textbox" name="textbox"></textarea>
    </div>
    ```

---

### Final HTML:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <title>Accessibility Quiz</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header>
      <img id="logo" alt="freeCodeCamp" src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg">
      <h1>HTML/CSS Quiz</h1>
      <nav>
        <ul>
          <li><a accesskey="i" href="#student-info">INFO</a></li>
          <li><a accesskey="h" href="#html-questions">HTML</a></li>
          <li><a accesskey="c" href="#css-questions">CSS</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="student-name">Name:</label>
            <input type="text" name="student-name" id="student-name" />
          </div>
          <div class="info">
            <label for="student-email">Email:</label>
            <input type="email" name="student-email" id="student-email" />
          </div>
          <div class="info">
            <label for="birth-date">Date of Birth:</label>
            <input type="date" name="birth-date" id="birth-date" />
          </div>
        </section>
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>1</h3>
            <fieldset class="question" name="html-question-one">
              <legend>
                The legend element represents a caption for the content of its
                parent fieldset element
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" name="q1" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" name="q1" value="false" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" name="q2" value="true" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" name="q2" value="false" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
        </section>
        <section role="region" aria-labelledby="css-questions">
          <h2 id="css-questions">CSS</h2>
          <div class="formrow">
            <div class="question-block">
              <label for="selector">Can the CSS margin property accept negative values?</label>
            </div>
            <div class="answer">
              <select name="selector" id="selector" required>
                <option value="">Select an option</option>
                <option value="yes">Yes</option>
                <option value="no">No</option>
              </select>
            </div>
            <div class="question-block">
              <label for="css-textarea">Do you have any questions:</label>
            </div>
            <div class="answer">
              <textarea id="css-textarea" name="css-questions" rows="5" cols="24"></textarea>
            </div>
          </div>
        </section>
        <button type="submit">Send</button>
      </form>
    </main>
    <footer>
      <address>
        <a href="https://freecodecamp.org">freeCodeCamp</a><br />
        San Francisco<br />
        California<br />
        USA
      </address>
    </footer>
  </body>
</html>
```

### Final CSS:

```css
@media (prefers-reduced-motion: no-preference) {
  * {
    scroll-behavior: smooth;
  }
}

body {
  background: #f5f6f7;
  color: #1b1b32;
  font-family: Helvetica;
  margin: 0;
}

header {
  width: 100%;
  height: 50px;
  background-color: #1b1b32;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
}

#logo {
  width: max(10rem, 18vw);
  background-color: #0a0a23;
  aspect-ratio: 35 / 4;
  padding: 0.4rem;
}

h1 {
  color: #f1be32;
  font-size: min(5vw, 1.2em);
  text-align: center;
}

nav {
  width: 50%;
  max-width: 300px;
  height: 50px;
}

nav > ul {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: center;
  padding-inline-start: 0;
  margin-block: 0;
  height: 100%;
}

nav > ul > li {
  color: #dfdfe2;
  margin: 0 0.2rem;
  padding: 0.2rem;
  display: block;
}

nav > ul > li:hover {
  background-color: #dfdfe2;
  color: #1b1b32;
  cursor: pointer;
}

li > a {
  color: inherit;
  text-decoration: none;
}

main {
  padding-top: 50px;
}

section {
  width: 80%;
  margin: 0 auto 10px auto;
  max-width: 600px;
}

h1,
h2 {
  font-family: Verdana, Tahoma;
}

h2 {
  border-bottom: 4px solid #dfdfe2;
  margin-top: 0px;
  padding-top: 60px;
}

.info {
  padding: 10px 0 0 5px;
}

.formrow {
  margin-top: 30px;
  padding: 0px 15px;
}

input {
  font-size: 16px;
}

.info label, .info input {
  display: inline-block;
}

.info input {
  width: 50%;
  text-align: left;
}

.info label {
  width: 10%;
  min-width: 55px;
  text-align: right;
}

.question-block {
  text-align: left;
  display: block;
  width: 100%;
  margin-top: 20px;
  padding-top: 5px;
}

h3 {
  margin-top: 5px;
  padding-left: 15px;
  font-size: 20px;
}

h3::before {
  content: "Question #";
}

.question {
  border: none;
  padding-bottom: 0;
}

.answers-list {
  list-style: none;
  padding: 0;
}

button {
  display: block;
  margin: 40px auto;
  width: 40%;
  padding: 15px;
  font-size: 23px;
  background: #d0d0d5;
  border: 3px solid #3b3b4f;
}

footer {
  background-color: #2a2a40;
  display: flex;
  justify-content: center;
}

footer,
footer a {
  color: #dfdfe2;
}

address {
  text-align: center;
  padding: 0.3em;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
```

---

**Final output**:

![OUTPUT Image](https://github.com/user-attachments/assets/870e1885-183d-4689-be24-76d24557c464)




 
