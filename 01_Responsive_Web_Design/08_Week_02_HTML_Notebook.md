# HTML Learning Journey Notebook  
**Source:** [freeCodeCamp.org](https://www.freecodecamp.org)  
**Project:** Learn Typography by Building a Nutrition Label  

---

### HTML and CSS Step-by-Step Guide  

#### Basic Setup  
- **Basic structure:**  
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
  <p>Serving size 2/3 cup (55g)</p>
</body>
</html>
```

- **Adding external styles and fonts:**  
```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800">
<link rel="stylesheet" href="styles.css">
```

- **Set body font:**  
```css
body {
  font-family: "Open Sans", sans-serif;
}
```

- **HTML root font-size:**  
```css
html {
  font-size: 16px;
}
```

#### Creating the Label Layout  
- **Wrap the content in a div:**  
```html
<div class="label">
</div>
```

- **CSS for `.label` div:**  
```css
.label {
  border: 2px solid black;
  width: 270px;
  margin: 20px auto;
  padding: 0 7px;
}
```

- **Reset box model:**  
```css
* {
  box-sizing: border-box;
}
```

- **Styling the `h1` element:**  
```css
h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}
```

- **Remove paragraph margins:**  
```css
p {
  margin: 0;
}
```

#### Adding Dividers and Sections  
- **Add a divider below the `h1` tag:**  
```html
<div class="divider"></div>
```

- **CSS for `.divider`:**  
```css
.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}
```

- **Update serving size paragraph:**  
```html
<p class="bold">Serving size <span>2/3 cup (55g)</span></p>
```

- **Bold class CSS:**  
```css
.bold {
  font-weight: 800;
}
```

- **Adding calories info section:**  
```html
<div class="calories-info">
  <div class="left-container">
    <h2 class="bold small-text">Amount per serving</h2>
    <p>Calories</p>
  </div>
  <span>230</span>
</div>
```

- **Styling the calories info:**  
```css
.calories-info {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}
.left-container p {
  margin: -5px -2px;
  font-size: 2em;
  font-weight: 700;
}
.calories-info span {
  margin: -7px -2px;
  font-size: 2.4em;
  font-weight: 700;
}
```

#### Adding Nutrient Values  
- **Creating daily value section:**  
```html
<div class="daily-value small-text">
  <p class="bold right no-divider">% Daily Value *</p>
  <div class="divider"></div>
  <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
  <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
</div>
```

- **Indent for sub-nutrient:**  
```css
.indent {
  margin-left: 1em;
}
```

- **Adjusting divider for specific elements:**  
```css
.daily-value p:not(.no-divider) {
  border-bottom: 1px solid #888989;
}
```

- **Italicize trans fat value:**  
```html
<p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
```

#### Final Elements  
- **Remaining nutrient values:**  
```html
<p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
<p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
<p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
<p class="indent no-divider">Dietary Fiber 4g</p>
<div class="divider"></div>
<p class="indent no-divider">Total Sugars 12g</p>
<div class="divider"></div>
<p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
<p class="indent no-divider"><span class="bold">Protein</span> 3g</p>
<div class="divider large"></div>
<p>Vitamin D 2mcg <span>10%</span></p>
<p>Calcium 260mg <span>20%</span></p>
<p>Iron 8mg <span>45%</span></p>
<p class="no-divider">Potassium 235mg <span>6%</span></p>
```

#### Note Section  
- **Add nutrition note:**  
```html
<p class="note">* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.</p>
```

- **CSS for `.note`:**  
```css
.note {
  font-size: 0.6rem;
  margin: 5px 0;
  padding: 0 8px;
  text-indent: -8px;
}
```

---

**Final HTML Structure:**

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800">
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <div class="label">
    <header>
      <h1 class="bold">Nutrition Facts</h1>
      <div class="divider"></div>
      <p>8 servings per container</p>
      <p class="bold">Serving size <span>2/3 cup (55g)</span></p>
    </header>
    <div class="divider large"></div>
    <div class="calories-info">
      <div class="left-container">
        <h2 class="bold small-text">Amount per serving</h2>
        <p>Calories</p>
      </div>
      <span>230</span>
    </div>
    <div class="divider medium"></div>
    <div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span class="bold">Cholesterol</span> 0mg <span class="bold">0%</span></p>
      <p><span class="bold">Sodium</span> 160mg <span class="bold">7%</span></p>
      <p><span class="bold">Total Carbohydrate</span> 37g <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <p class="indent no-divider"><span class="bold">Protein</span> 3g</p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
      <p>Calcium 260mg <span>20%</span></p>
      <p>Iron 8mg <span>45%</span></p>
      <p class="no-divider">Potassium 235mg <span>6%</span></p>
    </div>
    <div class="divider medium"></div>
    <p class="note">* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.</p>
  </div>
</body>

</html>
```

---

**Final output**:

![Nutrition Facts](https://github.com/user-attachments/assets/e43825ef-9c31-4b32-ad80-ab7f8e8f1648)

