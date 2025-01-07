# Bootstrap CSS Framework Lecture

## Section 1: Introduction to Bootstrap

### 1.1 What is Bootstrap?
Bootstrap is a front-end framework aimed at accelerating web development. It provides a set of pre-built responsive grid systems, components, and utilities that make it easy to create responsive websites with minimal custom CSS.

**Key Features:**
- **Responsive Design**: Automatically adjusts layouts based on screen size.
- **Pre-built Components**: Includes reusable elements like buttons, navigation bars, modals, forms, etc.
- **Customizable**: Modify the default Bootstrap theme using variables or the customization tool.
- **Cross-browser Compatibility**: Works across modern browsers.

---

## Section 2: Installation Guide

### 2.1 Prerequisites
**Tools:**
- **Code Editor**: Visual Studio Code (VS Code) or any preferred editor.
- **Web Browser**: Google Chrome, Mozilla Firefox, or other modern browsers.

### 2.2 Installing Bootstrap
**Installation Options:**
1. **Via CDN**: Simplest method by linking to Bootstrap's hosted CSS and JavaScript files.
2. **Via NPM**: Suitable for Node.js-based environments.
3. **Download**: Download compiled files and link them in the HTML.

**Example Code for CDN Integration:**

```html
<!-- Bootstrap CSS -->

- link this in the <head> tag

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">

<!-- Bootstrap JS -->
 
 - link this in the <body> tag

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" crossorigin="anonymous"></script>
```

---

## Section 3: Basic Usage and Components

### 3.1 Layout and Grid System

**Grid System:**
Bootstrap uses a 12-column grid to define layouts. Developers can set column widths using grid classes like `col-12`, `col-sm-6`, etc.

**Example Layout:**
```html
<div class="container">
  <div class="row">
    <div class="col-12 col-md-6">Column 1</div>
    <div class="col-12 col-md-6">Column 2</div>
  </div>
</div>
```

**Breakpoints:**
- `col-sm-`: Small devices (≥ 576px)
- `col-md-`: Medium devices (≥ 768px)
- `col-lg-`: Large devices (≥ 992px)
- `col-xl-`: Extra-large devices (≥ 1200px)

### 3.2 Typography in Bootstrap

**Typography Classes:**
- `display-*`, `lead`, `text-muted`, `text-center` for various text styles.

**Example:**
```html
<h1 class="display-1">Heading</h1>
<p class="lead">Lead paragraph</p>
<p class="text-muted">Muted text</p>
```

### 3.3 Colors and Backgrounds

**Utility Classes for Colors:**
- Text colors: `text-primary`, `text-danger`
- Background colors: `bg-warning`, `bg-success`

**Example:**
```html
<p class="text-primary">This is primary colored text</p>
<p class="bg-warning text-dark">This is a warning background</p>
```

---

## Section 4: Components

### 4.1 Buttons

Bootstrap provides several button classes like `btn-primary`, `btn-secondary`, `btn-success`, etc.

**Example:**
```html
<button class="btn btn-primary">Primary Button</button>
<button class="btn btn-secondary">Secondary Button</button>
```

### 4.2 Navigation Bar

The navbar component is flexible and responsive.

**Example:**
```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Navbar</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Features</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Pricing</a>
      </li>
    </ul>
  </div>
</nav>
```

### 4.3 Cards

The card component is a flexible container for content like images, titles, text, and links.

**Example:**
```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```

---

## Section 5: Utilities

### 5.1 Spacing and Sizing

Bootstrap provides utilities for margin and padding.
- **Padding**: `p-{size}`
- **Margin**: `m-{size}`

**Example:**
```html
<div class="p-3">Padding 3</div>
<div class="m-4">Margin 4</div>
```

### 5.2 Flexbox Utilities

Flexbox utilities allow you to align and distribute items easily.

**Example:**
```html
<div class="d-flex justify-content-center">
  <div class="p-2">Flex Item 1</div>
  <div class="p-2">Flex Item 2</div>
</div>
```

### 5.3 Responsive Design

Use responsive utility classes like `d-none d-sm-block` or `d-block d-md-none` to show/hide elements based on screen sizes.

**Example:**
```html
<div class="d-none d-sm-block">Visible on small screens and up</div>
<div class="d-block d-md-none">Visible only on medium and smaller screens</div>
```

---

## Section 6: JavaScript Components

### 6.1 Modals

Modals are useful for creating dialog boxes, forms, or notifications. They require Bootstrap's JavaScript components.

**Example:**
```html
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
  Launch demo modal
</button>
<div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        Content goes here.
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

---

## Section 7: Final Project Task

**Task:** Build a Portfolio Page using Bootstrap.

**Requirements:**
- **Header with Navigation**: Use the Bootstrap Navbar component for responsive navigation.
- **Hero Section**: Implement a full-width hero section with a call-to-action button.
- **Flexbox Layout for Services or Skills**: Use Bootstrap's flex utilities to lay out services or skills.
- **Grid Layout for Portfolio Items**: Use the grid system to display portfolio items responsively.
- **Footer**: Create a footer with social media links and contact information using the grid system and utility classes.
