# Code Explanation - Be Profitable With Futures Project

This document explains the code structure behind the "Be Profitable With Futures" project, including HTML elements and where to modify images.

## HTML Structure Explained

HTML (HyperText Markup Language) is the standard markup language for documents designed to be displayed in a web browser. Here's an explanation of the key HTML elements used throughout this project:

### Basic HTML Elements

- `<!DOCTYPE html>`: Declaration that defines this document as HTML5
- `<html lang="en">`: Root element of the HTML page, with "en" specifying English language
- `<head>`: Container for metadata (data about data) and is placed between the `<html>` tag and the `<body>` tag
- `<meta>`: Provides metadata about the HTML document, such as character encoding and viewport settings
- `<title>`: Defines the title of the document shown in the browser's title bar
- `<link>`: Links to external resources like CSS files
- `<script>`: Contains or points to JavaScript code
- `<body>`: Contains all the content that displays on the page

### Structural Elements

- `<header>`: Represents introductory content, typically a banner area at the top of the page
- `<nav>`: Defines a section of navigation links
- `<main>`: Specifies the main content of the document
- `<section>`: Defines a section in a document
- `<footer>`: Represents a footer for a document or section

### Content Elements

- `<h1>`, `<h2>`, `<h3>`, etc.: Heading elements, with `<h1>` being the most important and `<h6>` the least
- `<p>`: Paragraph element
- `<ul>`: Unordered list
- `<ol>`: Ordered list
- `<li>`: List item
- `<a>`: Anchor element for creating hyperlinks
- `<blockquote>`: Indicates that the enclosed text is an extended quotation
- `<strong>`: Indicates strong importance, typically displayed as bold text
- `<em>`: Emphasizes text, typically displayed as italic
- `<span>`: Generic inline container for styling purposes
- `<i>`: Used for icons with Font Awesome

### Container and Layout Elements

- `<div>`: Generic container for flow content, used extensively for layout and styling
- `<div class="...">`: Divs with class attributes for specific styling and functionality
- `<canvas>`: Used for drawing graphics via JavaScript (for charts in this project)
- `<table>`: Creates a table
- `<tr>`: Table row
- `<th>`: Table header cell
- `<td>`: Table data cell

## CSS Classes Explained

The project uses numerous CSS classes to style elements. Here are some of the most important ones:

- `.header-content`: Styles for the header section content
- `.subtitle`: Styles for subtitle text
- `.section`: Styles for main content sections
- `.hero-section`: Styles for the hero banner on the home page
- `.evidence-card`: Styles for cards displaying evidence
- `.pillar`: Styles for the three pillars of trading (risk management, psychological discipline, technical analysis)
- `.counter-card`: Styles for counterargument cards
- `.navigation-buttons`: Styles for navigation buttons between pages
- `.footer-content`: Styles for footer content

## JavaScript Functionality

The `script.js` file contains JavaScript code that powers the interactive elements:

- Chart.js implementations for data visualization
- Risk meter slider functionality
- Emotional cycle chart
- Trading chart simulation
- Survival simulation chart

## Where to Change Images

### Home Page (index.html)

- **Hero Background**: Line 45 in `styles.css` - Change the URL in:
  ```css
  .landing-page .hero-section {
      background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('images/hero-bg.jpg');
  }
  ```

### Current Knowledge Page (current-knowledge.html)

- **Perception Image**: Line 79 - Change the `src` attribute:
  ```html
  <img src="images/perception.png" alt="Trading perception" class="perception-img">
  ```
- **Reality Image**: Line 87 - Change the `src` attribute:
  ```html
  <img src="images/reality.png" alt="Trading reality" class="reality-img">
  ```

### Contact Page (contact.html)

- **Author Image**: The contact page uses an image of Rhys at line 79:
  ```html
  <div class="author-image">
      <img src="images/pfpofrhys.jpg" alt="Rhys Paulk" class="author-photo">
  </div>
  ```
  To change this image, replace "pfpofrhys.jpg" with your own image file name. The CSS for this image is already set up in styles.css:
  ```css
  .author-photo {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      object-fit: cover;
  }
  ```

## Adding New Images

To add new images to the project:

1. Place your image files in the `images/` directory
2. Reference them in HTML using the `<img>` tag:
   ```html
   <img src="images/your-image.jpg" alt="Description of image" class="your-class">
   ```
3. Or reference them in CSS as backgrounds:
   ```css
   .your-element {
       background-image: url('images/your-image.jpg');
   }
   ```

## Chart Customization

The charts are created using Chart.js in the script.js file. To modify the charts:

1. **Emotion Chart**: Find the `createEmotionChart()` function in script.js
2. **Trading Chart**: Find the `createTradingChart()` function in script.js
3. **Survival Chart**: Find the `createSurvivalChart()` function in script.js

## Form Functionality

The contact form in contact.html is currently set up for display purposes only. To make it functional:

1. Add a form action and method:
   ```html
   <form action="your-form-handler" method="post">
   ```
2. Implement a form handler on your server or use a service like Formspree

## Responsive Design

The website is designed to be responsive across different screen sizes. The responsive behavior is controlled by media queries at the end of the styles.css file:

```css
@media (max-width: 768px) {
    /* Tablet styles */
}

@media (max-width: 480px) {
    /* Mobile styles */
}
```

## File Structure

```
AP Lang Project/
├── images/
│   ├── hero-bg.jpg
│   ├── perception.png
│   └── reality.png
├── index.html
├── current-knowledge.html
├── thesis.html
├── evidence.html
├── risk-management.html
├── psychological-discipline.html
├── technical-analysis.html
├── counterarguments.html
├── significance.html
├── contact.html
├── styles.css
├── script.js
├── README.md
└── CODE_README.md (this file)
```

## How to Modify Content

1. Open the relevant HTML file in a text editor
2. Find the section you want to modify
3. Edit the content between the appropriate HTML tags
4. Save the file and refresh the browser to see changes

## Common HTML Patterns Used in This Project

### Section Pattern
```html
<section class="section">
    <h2>Section Title</h2>
    <p>Section content goes here.</p>
    <!-- More content elements -->
</section>
```

### Card Pattern
```html
<div class="card-type">
    <div class="card-header">
        <h3>Card Title</h3>
    </div>
    <div class="card-body">
        <p>Card content goes here.</p>
    </div>
</div>
```

### Navigation Pattern
```html
<div class="navigation-buttons">
    <a href="previous-page.html" class="nav-button back">
        <i class="fas fa-arrow-left"></i> Back
    </a>
    <a href="next-page.html" class="nav-button next">
        Next <i class="fas fa-arrow-right"></i>
    </a>
</div>
```

This documentation should help you understand and modify the code behind the "Be Profitable With Futures" project.
