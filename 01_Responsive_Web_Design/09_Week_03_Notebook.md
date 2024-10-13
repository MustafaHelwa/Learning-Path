# HTML and CSS Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org) and other references.  
**Project:** Learn Accessibility by Building a Quiz

---

### HTML and CSS Step-by-Step Guide

#### Basic Setup

- Starting with the basic html and css code: 

Html:
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



css:
body {
  background: #f5f6f7;
  color: #1b1b32;
  font-family: Helvetica;
  margin: 0;
}

- use `#logo` selector to set a maximum width for it of `10rem` or `18vw`. Also, add color to the background, `aspect-ratio` of `35 / 4` and a `padding`:
  #logo{
  width: max(10rem, 18vw);
  background-color: #0a0a23;
  aspect-ratio: 35 / 4;
  padding: 0.4rem; 
  }

- Now, use a `header` selector to adjust header styling as below:
  header{
  width: 100%;
  height: 50px;
  background-color: #1b1b32;
  display: flex; 
  }

- Then, adjuts `h1` font size and color:
  h1{ 
  color: #f1be32; 
  font-size: min(5vw, 1.2em);
  }

- Inside <nav> element, create an unordered list of three elements:
        <nav>
        <ul>
          <li><a>INFO</a></li>
          <li><a>HTML</a></li>
          <li><a>CSS</a></li>
          </ul>
      </nav>

- Use The child combinator selector `>` to target only elements that are matching the second selector and are **a direct** child of the first selector:
  nav > ul{
  justify-content: space-evenly;
  display: flex;
  }

- inside the <main> element, insert a form that posts to the required link and make three sections within it:
     <main>
      
        <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
          <section>
            </section>
            <section>
              </section>
              <section>
                </section>
          </form>
        
    </main>

- Use `role` attribute to indicate the purpose of each element (WAI), make <section> role as `region`:
          <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region"></section>
        <section role="region"></section>
        <section role="region"></section>
      </form>

- Add the following `aria-labelledby` attributes to the `section` elements with the needed <h2> elements for each :

        <section role="region" aria-labelledby="student-info"><h2 id="student-info">Student Info</h2></section>
        <section role="region" aria-labelledby="html-questions"><h2 id="html-questions">HTML</h2></section>
        <section role="region" aria-labelledby="css-questions"><h2 id="css-questions">CSS</h2></section>

- Set a `font-family` for <h1> and <h2>. Also, add a backup font next to it. Then add a bottom border below <h2>:
  h1, h2{
  font-family: Verdana Tahoma;
    
    }
    h2{
    border-bottom: 4px solid #dfdfe2;
    }

- Reference each <a> in the <li> element of <ul> list to the correspondent `id` using `href`:
          <ul>
          <li><a href="#student-info">INFO</a></li>
          <li><a href="#html-questions">HTML</a></li>
          <li><a href="#css-questions">CSS</a></li>
          </ul>


- Next, add three <div> elements and nest one <label> and one <input> elements within each <div>:
          <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label></label>
            <input />
          </div>
          <div class="info">
            <label></label>
            <input />
          </div>
          <div class="info">
            <label></label>
            <input />
          </div>
        </section>

- Make a `for` attribute for each <label> element and link it with the corresponding <input> through `id` attribute:

          <section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="student-name">Name:</label>
            <input id="student-name" />
          </div>
          <div class="info">
            <label for="emailadd">Email:</label>
            <input id="emailadd"/>
          </div>
          <div class="info">
            <label for="dob">Date of Birth:</label>
            <input id="dob"/>
          </div>
        </section>

- Give a `name` attribute for each <input> element:

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

- Note that you can give a `placeholder` attribute for `Name` input:                  <input type="text" name="student-name" id="student-name" placeholder="e.g. Omar Ali" />
- Add two <div> elements and number them using <h3> element, wrap the number with Append a <span> element with a `class` of `sr-only` to each of the <h3> elements. then add a <fieldset> below the number. Give them appropriate class:
        </section>
        <section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <h3>1</h3>
            <fieldset class="question"></fieldset>
          </div>
          <div class="question-block">
            <h3>2</h3>
            <fieldset class="question"></fieldset>
          </div>
        </section>
              

- Add an `id` to each <input> to be able to link each question-answer using unique label then Use `for` attr to link each input to the label:
                   <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1"/>
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" />
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
                    <input type="radio" id="q2-a1" />
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" />
                  </label>
                </li>
              </ul>


    - Give each <input> element a `value` attribute matching the choice text:
                    <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    
                    <input type="radio" id="q1-a1" value="True"/> True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" value="False"/> False
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
                    <input type="radio" id="q2-a1" value="True"/> True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" value="False"/> False
                  </label>
                </li>
              </ul>


  - You will notice that you can pick 2 radio answers for the same question. To solve this problem, give the same `name` attribute for each 2 <input> elements:
                  <ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" value="true" name="q1a"/>
                    True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" value="false" name="q1a"/>
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
                    <input type="radio" id="q2-a1" value="true" name="q2a"/>
                    True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" value="false" name="q2a"/>
                    False
                  </label>
                </li>
              </ul>

- target each `before` pseudo-element of <h3> element and give it a `content` of `"Question #"`:
  h3::before {
  content: "Question #";

}

- 
      
