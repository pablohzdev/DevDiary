# Introduction to HTML: How It Is Structured

All HTML documents share the same basic structure, often referred to as the **HTML boilerplate**. This structure must be in place before any meaningful content can be displayed in the browser.

By convention, `index.html` is the file that web servers look for by default when loading a website.

## Main Parts of an HTML Document

An HTML document is composed of several essential parts that define how the browser interprets and displays the page.

## DOCTYPE Declaration

Every HTML page starts with a **doctype declaration**.

The purpose of the doctype is to tell the browser which version of HTML should be used to render the document. The current and latest standard is **HTML5**, and its doctype is very simple:

```html
<!DOCTYPE html>
```

Older versions of HTML used much more complex doctypes. For example, HTML 4.01:

```html
<!DOCTYPE HTML PUBLIC “-//W3C//DTD HTML 4.01 Transitional//EN” “http://www.w3.org/TR/html4/loose.dtd”>
```

In modern web development, we almost never use older HTML versions, so we will always use the HTML5 doctype.


## HTML Element (Root Element)

After declaring the doctype, we define the **HTML element**, which acts as the **root element** of the document. Every other element in the page is a descendant of this element.

Basic structure:

```html
<!DOCTYPE html>
<html lang=“en”>
</html>
```

### The `lang` Attribute

The `lang` attribute is an **HTML attribute** associated with the HTML element. Attributes provide additional information about an element.

#### What is the `lang` attribute?

The `lang` attribute specifies the language of the text inside the element. It is mainly used to improve **accessibility**.

Assistive technologies, such as screen readers, rely on this attribute to:

- Detect the language of the content
- Apply correct pronunciation rules
- Improve the overall user experience for multilingual users

## Head Element

The **head element** contains important meta-information about the webpage and resources required for the page to render correctly.

Inside the head, we should **not place any content that is meant to be displayed on the page**.

Example:

```html
<!DOCTYPE html>
<html lang=“en”>
<head>
<meta charset=“UTF-8”>
<title>Test webpage</title>
</head>
</html>
```

## Meta Element

The `meta` element is used to define metadata about the webpage.

We should always include the following meta tag inside the head:

```html
<meta charset=“UTF-8”>
```

Setting the character encoding is extremely important because it ensures that special characters and symbols from different languages are displayed correctly in the browser.

## Title Element

Another essential element inside the head is the **title element**:

```html
<title>Test webpage</title>
```

The title element provides a human-readable name for the webpage. This title appears in the browser tab.

For example, the text shown in your current browser tab corresponds to the title of the loaded HTML document.

If no title element is provided, the browser will usually default to using the file name as the page title.

## Body Element

The final required element in the HTML boilerplate is the **body element**.

This is where all visible content goes, including:

- Text
- Images
- Lists
- Links
- Buttons
- And other interactive elements

To complete the HTML boilerplate, the body element is placed inside the HTML element and always **below the head element**.

Full boilerplate example:

```html
<!DOCTYPE html>
<html lang=“en”>
<head>
<meta charset=“UTF-8”>
<title>Test webpage</title>
</head>
<body>

</body>
</html>
```