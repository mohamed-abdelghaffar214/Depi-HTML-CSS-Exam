# Question 1

## 1- Explain :has() pseudo-class

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

## 2- What is CSS aspect-ratio property?

The `aspect-ratio` property is used in reponsive layouts so that the width and height always have the same ratio, even when they change.

```css
img.profile-pic {
    aspect-ratio: 2 / 3;
}
```

## 3- How would you optimize CSS for performance?

I would minimize CSS files, use CSS variables, and avoid using properties and functions that deplete performance like `text-shadow`, `text-stroke`, `box-shadow`, `nth-child()`.

## 4- What are CSS Custom Properties (Variables) and their advantages over Sass variables?

CSS variables are custom values given names by the programmer, to be used by invoking these names anywhere in the document. They can have different values for different elements, but Sass variables only have one value at a time.

```css
:root {
    --text-success: #4BB543;
}
button.green-btn {
    color: var(--text-success);
}
```

## 5- If the width of the container is 500 pixels, what would the width of the three columns be in this layout?

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

## 6- What is the Critical Rendering Path?

The Critical Rendering Path is the sequence of steps that the browser goes through to convert the HTML, CSS, and Javascript into pixels on the screen.

## 7- What is the purpose of the CSS `clamp()` function?

The `clamp()` function sets minimum, preferred and maximum values to the property. It is used to maximize responsiveness by limiting the value to a specific range, and choosing a preferred value.

```css
p {
    font-size: clamp(1rem, 1.4rem, 3rem);
}
```
