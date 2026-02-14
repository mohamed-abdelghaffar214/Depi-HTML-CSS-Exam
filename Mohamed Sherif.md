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
