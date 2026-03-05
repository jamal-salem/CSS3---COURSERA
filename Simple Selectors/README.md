# CSS Selectors: Element, Class, and ID

Understanding selectors is fundamental in CSS.  
Selectors determine **which HTML elements** a CSS rule will apply to.

---

## 1. Element Selector

### Concept
Targets all elements of a specific HTML tag.

### Syntax
```css
p {
  color: blue;
}
```

### What Happens?
All `<p>` elements in the document will have blue text.

### When to Use
- Applying global styles
- Styling all elements of the same type
- Setting default typography

### Characteristics
- Simple
- Broad impact
- Lowest specificity

---

## 2. Class Selector

### Concept
Targets elements that share the same `class` attribute.

### HTML Example
```html
<p class="highlight">Hello</p>
```

### CSS Example
```css
.highlight {
  color: red;
}
```

### What Happens?
Any element with `class="highlight"` will have red text.

### Key Advantages
- Reusable
- Flexible
- Can be applied to multiple elements

### Example with Multiple Elements
```html
<div class="box"></div>
<div class="box"></div>
```

```css
.box {
  background-color: yellow;
}
```

Both elements will be styled.

### Specificity Level
Medium

---

## 3. ID Selector

### Concept
Targets a single unique element using the `id` attribute.

### HTML Example
```html
<div id="header">Welcome</div>
```

### CSS Example
```css
#header {
  background-color: black;
}
```

### What Happens?
Only the element with `id="header"` will be styled.

### Important Rules
- Must be unique in a page
- Should not be reused
- Highest specificity among basic selectors

### Specificity Level
High

---

## Specificity Hierarchy

When multiple rules target the same element, CSS applies the most specific one.

Priority Order:

ID Selector > Class Selector > Element Selector

### Example
```css
p {
  color: blue;
}

.text {
  color: green;
}

#main {
  color: red;
}
```

```html
<p id="main" class="text">Hello</p>
```

Final Result:
The text will be **red** because the ID selector overrides the others.

---

## Quick Comparison

| Selector Type | Symbol | Reusable | Specificity |
|--------------|--------|----------|------------|
| Element      | none   | Yes      | Low        |
| Class        | .      | Yes      | Medium     |
| ID           | #      | No       | High       |

---

## Engineering Perspective

- Use **Element selectors** for global structure.
- Use **Class selectors** for reusable styling patterns.
- Use **ID selectors** for unique components or layout anchors.

Mastering these three selectors is essential before moving to advanced CSS concepts like combinators, specificity calculation, and inheritance.
