# 🎨 CSS Foundations Notes

A summary of core CSS concepts I practiced during the Foundations section of The Odin Project.

---

## 🧱 Box Model & Layout Behavior

### 📦 `box-sizing: border-box`

Set this globally to make element dimensions easier to manage — padding and borders stay **inside** the defined width/height.

```css
* {
  box-sizing: border-box;
}
```

---

### 📐 Margins

- **Positive margins** push the element **away** from others  
- **Negative margins** pull the element **toward** (or into) others — can cause overlap

```css
margin-top: -10px; /* pulls the element up */
```

- To center horizontally (when width is set):

```css
margin: 0 auto;
```

- Shorthand:

```css
margin: 16px auto; /* Top & bottom: 16px; left & right: auto (centered) */
```

---

### 🧲 Collapsing Margins

- Adjacent vertical margins (like `margin-bottom` and `margin-top`) can collapse — only the **larger** value is used  
- Horizontal margins do **not** collapse

---

## 🧱 Display Types

### 🔹 `display: block`

- Takes **full width** of the parent  
- Starts on a **new line**  
- Respects padding, borders, and vertical margins

### 🔹 `display: inline`

- Stays **in-line** with surrounding content  
- **Ignores width/height**, and vertical margins

### 🔹 `display: inline-block`

- Like `inline`, but **allows width and height**

```html
<span style="display: inline-block; width: 150px;">This has width!</span>
```

### 🔹 `display: none`

- Removes the element from the document flow — as if it doesn't exist

### 🔹 `display: flex`

- Turns the container into a **flexbox layout**  
- Child items align in a row by default  
- Great for centering or distributing space

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

## 📚 Styling Essentials

### ✨ List Styling

Remove bullets and indentation:

```css
ul {
  list-style-type: none;
  padding-left: 0;
}
```

Add space between list items:

```css
ul li {
  margin-bottom: 8px;
}
```

---

### ✍️ Text Styling

Italic + underline:

```css
.subtitle {
  font-style: italic;
  text-decoration: underline;
}
```

---

### 🧼 CSS Reset (Recommended)

Start every project with this reset to neutralize browser defaults:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

- Removes default spacing  
- Ensures consistent box sizing across all elements