# Lecture 1: Introduction to CSS – Styling the Web

## Overview:

1. What CSS is and why it's essential for web development.
2. The difference between Inline, Internal, and External CSS.
3. The syntax and structure of CSS, including selectors, properties, and values.
4. Basic styling concepts like colors, backgrounds, and typography.

---

## 1. What is CSS?

### Definition:
CSS stands for Cascading Style Sheets, and it is used to control the style and layout of HTML elements. While HTML provides the structure of a webpage, CSS gives it life by defining how elements should look and behave.

In simpler terms:
CSS = Style + Layout.

- **HTML**: Creates the structure (e.g., headings, paragraphs, images).
- **CSS**: Styles and arranges those structures (e.g., colors, fonts, spacing).

### Importance of CSS:

- **Separation of Concerns**: CSS separates content (HTML) from presentation (CSS). This helps in maintaining and updating the website's look without changing its structure.
- **Improves Readability**: CSS makes your website look more appealing and easy to navigate, which directly impacts user experience.
- **Responsiveness**: CSS makes websites responsive to different screen sizes, making them work across mobile, tablet, and desktop devices.

### Real-World Analogy:
Think of HTML as the frame of a house (the skeleton), and CSS is the interior design (colors, furniture, style). The frame stays the same, but the interior can be adjusted to look stylish and organized!

---

## 2. How CSS Works with HTML

When you build a webpage, you structure it with HTML and then use CSS to style it. CSS can be applied in three primary ways:

1. **Inline CSS** (within an HTML tag)
2. **Internal CSS** (within the `<style>` tag in the head of HTML)
3. **External CSS** (in a separate `.css` file linked to the HTML)

### Inline CSS:

Inline CSS is written directly inside HTML tags using the `style` attribute.

```html
<p style="color: blue; font-size: 20px;">This is a styled paragraph.</p>
```

**Advantages:**
- Quick and simple for small changes.

**Disadvantages:**
- Messy and difficult to maintain for large websites.
- Can override other styles, causing conflicts.

---

### Internal CSS:

Internal CSS is written within the `<style>` tag in the head section of the HTML document.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Internal CSS Example</title>
  <style>
    p {
      color: green;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <p>This is a styled paragraph using internal CSS.</p>
</body>
</html>
```

**Advantages:**
- Keeps styles together in one document.
- Good for smaller projects or testing styles.

**Disadvantages:**
- The style applies only to the current page.
- Not as maintainable for large projects.

---

### External CSS:

External CSS is the most efficient method, especially for large websites. You create a separate `.css` file and link it to the HTML.

**HTML File:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>External CSS Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <p>This is a styled paragraph using external CSS.</p>
</body>
</html>
```

**CSS File (styles.css):**

```css
p {
  color: red;
  font-size: 22px;
}
```

**Advantages:**
- Centralized styling: One `.css` file can be linked to multiple HTML pages.
- Makes large websites easier to maintain.
- Faster page load times (browser caches the CSS file).

**Disadvantages:**
- Requires an additional HTTP request to load the CSS file.

---

## 3. CSS Syntax: Selectors, Properties, and Values

### Syntax Structure:
A typical CSS rule consists of three parts:

1. **Selector**: Specifies which HTML elements to style.
2. **Property**: Defines the style you want to apply (e.g., color, font-size).
3. **Value**: Specifies the value of the property (e.g., red, 16px).

```css
selector {
  property: value;
}
```

For example:

```css
p {
  color: blue;
  font-size: 18px;
}
```

- **Selector**: `p` (targets the `<p>` element)
- **Property**: `color` (specifies the color)
- **Value**: `blue` (sets the color to blue)

### Common CSS Selectors:

1. **Type Selector (Element Selector):** Targets all elements of a specific type.

   ```css
   h1 {
     color: blue;
   }
   ```

2. **Class Selector:** Targets all elements with a specific class.

   ```css
   .myClass {
     background-color: yellow;
   }
   ```

3. **ID Selector:** Targets a specific element with an ID.

   ```css
   #myID {
     font-size: 24px;
   }
   ```

4. **Universal Selector:** Targets all elements on the page.

   ```css
   * {
     margin: 0;
     padding: 0;
   }
   ```

5. **Descendant Selector:** Targets elements inside other elements.

   ```css
   div p {
     color: red;
   }
   ```

6. **Pseudo-classes:** Targets elements in a specific state, like hover.

   ```css
   a:hover {
     color: orange;
   }
   ```

### CSS Properties and Values:

- **`color`**: Sets the color of the text (e.g., `red`, `#333`, `rgb(255, 0, 0)`).
- **`font-size`**: Sets the size of the text (e.g., `16px`, `1em`, `1.5rem`).
- **`background-color`**: Sets the background color of an element (e.g., `blue`, `#ffcc00`).
- **`border`**: Adds borders around an element (e.g., `1px solid black`).
- **`padding`**: Controls the inner space around the element's content.
- **`margin`**: Controls the outer space around the element.

---

## 4. Colors and Backgrounds

### Color Formats:

1. **Named Colors**: CSS supports common color names like `red`, `green`, `blue`, etc.
2. **HEX Colors**: Defines colors in hexadecimal format (e.g., `#ff5733`).
3. **RGB Colors**: Defines colors using the Red, Green, and Blue channels (e.g., `rgb(255, 0, 0)`).
4. **HSL Colors**: Defines colors based on Hue, Saturation, and Lightness (e.g., `hsl(0, 100%, 50%)`).

### Background Properties:

1. **`background-color`**: Sets the background color of an element.

   ```css
   body {
     background-color: lightblue;
   }
   ```

2. **`background-image`**: Sets an image as the background.

   ```css
   body {
     background-image: url('image.jpg');
   }
   ```

3. **`background-position`**: Specifies the position of the background image.

   ```css
   body {
     background-position: center center;
   }
   ```

4. **`background-repeat`**: Controls whether the background image repeats.

   ```css
   body {
     background-repeat: no-repeat;
   }
   ```

---

## 5. Typography – Fonts and Text Styling

CSS allows you to customize the appearance of text using properties like `font-family`, `font-size`, `line-height`, `letter-spacing`, and `text-align`.

### Font Properties:

1. **`font-family`**: Specifies the font of an element (e.g., `Arial`, `Verdana`).
2. **`font-size`**: Specifies the size of the text (e.g., `16px`, `1em`).
3. **`font-weight`**: Controls the thickness of the text (e.g., `bold`, `normal`).
4. **`font-style`**: Specifies the style of the font (e.g., `italic`, `normal`).

### Text Styling:

1. **`line-height`**: Controls the space between lines of text.
2. **`letter-spacing`**: Controls the spacing between letters.
3. **`text-align`**: Aligns the text inside an element (e.g., `left`, `center`, `right`).

---

## 6. Summary and Hands-On Exercise

By the end of this lecture, students should understand how to:

- Apply inline, internal, and external CSS to style their web pages.
- Work with basic CSS syntax, selectors, and properties.
- Style colors, backgrounds, and text using CSS.

### Exercise:

Create a simple HTML page and:

1. Use inline CSS to change the color of a heading.
2. Create an internal CSS block to change the background color of the body.
3. Link to an external CSS file and use it to style a paragraph.
