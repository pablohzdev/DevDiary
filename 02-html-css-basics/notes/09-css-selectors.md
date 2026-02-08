# CSS: Selectors  

## What is a selector?  

In CSS, a selector indicates which HTML elements a rule should apply to. In other words, is the way that we “select" the elements that we want to stylize.  

## Universal selector  

The universal selector targets **all elements** in a document. It is represented by an asterisk (`*`).  
In the example below, every element on the page would receive the style `color: purple;`.  

```css
* {
  color: purple;
}
```

## Type (element) selector  

A type selector (also called an element selector) selects all elements of a given HTML tag. Its syntax is simply the name of the element.  

Example HTML:  

```html
<div>Hello, World!</div>
<div>Hello again!</div>
<p>Hi...</p>
<div>Okay, bye.</div>
```

Example CSS:  

```css
div {
  color: white;
}
```

In this case, all three `<div>` elements would be styled, but the `<p>` element would not.  

## Class selectors  

Class selectors target all elements that share a specific class. A class is an attribute that you assign to an HTML element.  

Example HTML:  

```html
<div class="alert-text">Please agree to our terms of service.</div>
```

Example CSS:  

```css
.alert-text {
  color: red;
}
```

Class selectors are written using a period (`.`) followed immediately by the class name. Class names are case-sensitive.  

You can reuse the same class on multiple elements — classes are not unique.  

A class name **cannot start with a number** (for example, `1-element` would be invalid).  

You can assign multiple classes to a single element by separating them with spaces, like this:  
`class="alert-text severe-alert"`.  
Because spaces separate class names, multi-word class names should use hyphens instead of spaces.  

## ID selectors  

ID selectors work similarly to class selectors, but with an important difference: **an ID must be unique on a page**. No two elements should share the same ID. IDs also cannot contain spaces.  

Example HTML:  

```html
<div id="title">My page</div>
```

Example CSS:  

```css
#title {
  background-color: red;
}
```

Instead of a period, ID selectors use a hashtag (`#`) followed by the ID name.  

Many developers overuse IDs when a class would be enough. You should generally prefer classes unless you specifically need an ID (for example, for navigation links or very specific styling cases).  

Like classes, **IDs cannot begin with a number**.  

## Grouping selectors  

Sometimes different selectors share the same styles. Instead of repeating the same rules, we can group them using commas.  

Example without grouping:  

```css
.read {
    color: white;
    background-color: black;
}

.unread {
    color: white;
    background-color: black;
}
```

Example with grouping:  

```css
.read,
.unread {
    color: white;
    background-color: black;
}

.read {
    /* unique styles */
}

.unread {
    /* unique styles */
}
```

This reduces repetition and keeps the CSS cleaner.  

## Chaining selectors  

You can combine multiple selectors **without spaces** to target elements that match all of them at the same time.  

Example HTML:  

```html
<div>
    <div class="subsection header">Latest Posts</div>
    <p class="subsection preview">This is where a preview for a post might go.</p>
</div>
```

If we want to style only the element that has **both** `subsection` and `header`, we can chain the selectors:  

```css
.subsection.header {
    color: red;
}
```

This selects elements that contain **both** classes at the same time. Notice there is **no space** between them.  

You can also chain a class with an ID:  

Example HTML:  

```html
<div>
    <div class="subsection header">Latest Posts</div>
    <p class="subsection" id="preview">This is where a preview for a post might go.</p>
</div>
```

Example CSS:  

```css
.subsection.header {
    color: red;
}

.subsection#preview {
    color: blue;
}
```

Note: You **cannot chain two type selectors**, because an element cannot be two different HTML tags at the same time.  

## Descendant combinator  

Combinators describe relationships between selectors instead of just selecting elements directly.  

The **descendant combinator** is represented by a space between selectors. It selects elements that are inside another element, no matter how deeply nested they are.  

For example, `.ancestor .child` means:  
> “Select `.child` only if it is inside an element with class `.ancestor`.”  

Example HTML:  

```html
<div class="ancestor">
    <div class="contents">
        <div class="contents"></div>
    </div>
</div>

<div class="contents"></div>
```

Example CSS:  

```css
.ancestor .contents {
    /* styles */
}
```

In this case, the **first two** `.contents` elements would be selected, but the last one would not, because it is not inside `.ancestor`.  

You can chain multiple descendant selectors like `.one .two .three .four`, but this is generally not recommended because it can become hard to read and may cause specificity problems.  