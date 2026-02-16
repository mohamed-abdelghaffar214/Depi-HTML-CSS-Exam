# HTML and CSS Task by Mohamed Sherif

## Question 1

### 1- Explain :has() pseudo-class

The `:has()` pseudo-class matches a parent element by a specific sibling or a specific child element

```css
/* Match by a child */
h1.has(p) {
    text-decoration-line: underline;
}
/* Match by a sibling */
div.has(+ form) {
    display: flex;
}
/* Match by a child's class */
section.has(.container) {
    height: 120vh;
}
```

### 2- What is CSS aspect-ratio property?

The `aspect-ratio` property is used in reponsive layouts so that the width and height always have the same ratio, even when they change.

```css
img.profile-pic {
    aspect-ratio: 2 / 3;
}
```

### 3- How would you optimize CSS for performance?

I would minimize CSS files, use CSS variables, and avoid using properties and functions that deplete performance like `text-shadow`, `text-stroke`, `box-shadow`, `nth-child()`.

### 4- What are CSS Custom Properties (Variables) and their advantages over Sass variables?

CSS variables are custom values given names by the programmer, to be used by invoking these names anywhere in the document. They can have different values for different elements, but Sass variables only have one value at a time.

```css
:root {
    --text-success: #4BB543;
}
button.green-btn {
    color: var(--text-success);
}
```

### 5- If the width of the container is 500 pixels, what would the width of the three columns be in this layout?

```css
.grid {
    display: grid; 
    grid-template-columns: 50px 1fr 2fr;
}
```

1fr = (500 - 50) / 3 = 150

- First Column: 50px
- Second Column: 150px
- Third Column: 300px

### 6- What is the Critical Rendering Path?

The Critical Rendering Path is the sequence of steps that the browser goes through to convert the HTML, CSS, and Javascript into pixels on the screen.

### 7- What is the purpose of the CSS `clamp()` function?

The `clamp()` function sets minimum, preferred and maximum values to the property. It is used to maximize responsiveness by limiting the value to a specific range, and choosing a preferred value.

```css
p {
    font-size: clamp(1rem, 1.4rem, 3rem);
}
```

### 8- In the context of CSS performance, what is 'Layout Thrashing'?

Layout thrashing is a performance problem that happens when Javascript changes the layout and reads it multiple times in quick succession, causing the browser to recalculate layout every second.

### 9- What is the best way to code three choices within a form input so that the user can select only one item?

Dropdown menu is the best way, since it saves space in the form for other elements.

```html
<select id="choice" name="choice">
    <option value="placeholder">select</option>
    <option value="choice 1">One</option>
    <option value="choice 2">Two</option>
    <option value="choice 3">Three</option>
</select>
```

### 10- Using the :nth-child pseudo-class, what would be the most efficient way to style every third item in a list, no matter how many items are present, starting with item 2?

```css
li:nth-child(3n + 2) { }
```

---

## Question 2

### Code 1

Code 1 creates a picture element with different source images for widths more than 750px and 1000px, and another image for fallback

### Code 2

Code 2 sets the margin on the left to a value calculated by adding 5 pixels to 5% of the full width.

### Code 3

Same as Code 1

### Code 4

Code 4 creates a table with one row and three cells. the first one is a header containing the word "Header" and the other two contain 10 and 18 respectively.

---

## Question 3

### 1- The flex-direction property is used to specify the direction in which flex items are displayed. What are the values used to specify the direction of the items in the following examples?

- Example 1: row
- Example 2: row-reverse
- Example 3: column
- Example 4: column-reverse

### 2- Which element(s) will be blue?

`<p>` elements called P3 and P4 will be blue
