# CSS: Introduction  

## What is CSS?  

Before anything else, it’s important to understand that a web page is essentially a text document. In this document you write all your HTML code, which defines the structure and content of the page.  

CSS is a separate language that works alongside HTML. While HTML defines *what* is on the page, CSS is responsible for how it looks — including colors, layout, spacing, positioning, and overall visual style.  

## What does CSS mean?  

CSS stands for **Cascading Style Sheets**. The idea behind it is simple but very powerful: apply visual styles (such as colors, shapes, margins, and spacing) to one or multiple documents — usually HTML files — in an automatic and consistent way.  

A common approach is to have many HTML files but only one CSS file. Each HTML document links to this single stylesheet. This way, if you make a change in the CSS file, it will automatically affect all the connected web pages.  

## Why is CSS used?  

CSS allows us to separate content from presentation. This makes websites much easier to maintain and update over time.  

Instead of changing styles in every single HTML file, you can modify them in one central CSS file and have those changes reflected across the entire site. This also reduces repetition and keeps your code cleaner and more organized.  

## Basic syntax  

At its core, CSS consists of rules. Each rule contains:  
- A **selector**, which targets the HTML element you want to style.  
- One or more **declarations**, each made up of a property and a value.  

Example:  

```css
div.bold-text { /* selector */
    font-weight: 700; /* property: value */
}
```

## Semantic HTML  

A `<div>` is a basic HTML container element. By itself, it doesn’t have any meaning — it simply groups other elements together.  

Whenever possible, it’s better to use more meaningful (semantic) elements like `<h1>` for headings or `<p>` for paragraphs. However, there are many situations where you just need a general container to organize your layout, and that’s when `<div>` becomes useful.  

## Adding CSS to HTML

There are three main ways to include CSS in an HTML document.

### External CSS  

This is the most widely used approach. It consists of creating a separate `.css` file and connecting it to your HTML document inside the `<head>` section using a `<link>` element:

```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

The `href` attribute specifies the location of the CSS file — either an absolute URL or, more commonly, a path relative to your HTML file. The `rel` attribute is required because it defines the relationship between the HTML document and the linked file.

Note: You can name your CSS file anything you want as long as it ends in `.css`, though names like `styles.css` or `style.css` are the most common.


### Internal CSS  

Internal (or embedded) CSS means writing your styles directly inside the HTML file instead of using a separate stylesheet. You place all your CSS inside a `<style>` tag, which is usually located within the `<head>` section of the document. Because the styles are already inside the HTML file, you no longer need a `<link>` element.

```html
<head>
    <style>
        div {
            color: white;
            background-color: black;
        }

        p {
            color: red;
        }
    </style>
</head>
<body>
</body>
```

This method is useful when you only need styles for a single page, but it is not considered best practice for larger projects.


### Inline CSS  

Inline CSS allows you to apply styles directly to individual HTML elements using the `style` attribute. However, this method is generally discouraged:

```html
<body>
    <div style="color: white; background-color: black;">...</div>
</body>
```

In this case, no selectors are needed because the styles are written directly inside the HTML tag itself.

This approach is not recommended because:
- It can quickly become disorganized when many styles are applied to a single element.
- Inline styles override both internal and external CSS, which can lead to unexpected behavior.