# Combining CSS Selectors

Combining selectors allows you to target elements more precisely.
Instead of styling everything broadly, you can narrow down exactly which elements should be affected.

---

## 1. Grouping Selectors (Comma)

### Concept
Apply the same style to multiple selectors.

### Syntax
```css
h1, h2, p {
  color: blue;
}
```

### What Happens?
All `<h1>`, `<h2>`, and `<p>` elements will have blue text.

### When to Use
- Applying shared styles
- Reducing duplicate code
- Improving readability

---

## 2. Descendant Selector (Space)

### Concept
Target elements inside another element (at any depth).

### Syntax
```css
div p {
  color: red;
}
```

### Meaning
Select all `<p>` elements inside any `<div>`.

### Example
```html
<div>
  <p>This will be red</p>
</div>
```

### Use Case
- Styling elements within specific sections
- Scoping styles

---

## 3. Child Selector (>)

### Concept
Target only direct children.

### Syntax
```css
div > p {
  color: green;
}
```

### Meaning
Select `<p>` elements that are direct children of `<div>`.

### Difference from Descendant
- Descendant: any level deep
- Child: only one level down

---

## 4. Class Combination

### Concept
Target elements that have multiple classes.

### Syntax
```css
.box.highlight {
  background-color: yellow;
}
```

### Meaning
Select elements that have BOTH `box` and `highlight` classes.

### Example
```html
<div class="box highlight"></div>
```

---

## 5. Element + Class

### Concept
Target a specific element with a specific class.

### Syntax
```css
p.text {
  font-weight: bold;
}
```

### Meaning
Select only `<p>` elements with class="text".

---

## 6. ID + Class

### Syntax
```css
#main.box {
  color: white;
}
```

### Meaning
Select element with id="main" AND class="box".

---

## 7. Attribute Selector

### Syntax
```css
input[type="text"] {
  border: 1px solid black;
}
```

### Meaning
Select input elements where type="text".

---

# Specificity Reminder

When combining selectors, specificity increases.

Example:

div p         → low specificity
p.text        → higher
#main .box    → even higher

More precise selectors override general ones.

---

# Engineering Perspective

- Use grouping to reduce repetition.
- Use descendant selectors to scope styles.
- Use child selectors for structural precision.
- Combine classes for modular styling.
- Avoid overly complex selectors for maintainability.
