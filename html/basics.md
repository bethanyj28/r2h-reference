## What is HTML?

HTML is known as a **markup language**, which defines the content within the page. HTML consists of various elements which lets you control the appearance of content on the page.

## HTML elements
![Anatomy of an HTML element](grumpy-cat-small.png)

### Opening tag
This is the name of the element wrapped in angled brackets. It serves to show how the content should be formatted or treated.

### Closing tag
This is the same as the opening tag but with a forward slash before the element name. This serves to ensure there is no ambiguity for how the content should be treated.

### Content
This is the content of the element, which is text in this case.

### Element
The opening and closing tags with the content
[Here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) is a list of HTML elements.

### Attributes
![Attributes in HTML tag](grumpy-cat-attribute-small.png)
This is extra information about the element that shouldn't be included in the content.
[Here](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) is a list of HTML attributes and the elements they can affect.

## Nesting elements
Elements can be used inside other elements in what is known as nesting. For example, we can **bold** words using the `<strong>` element within a paragraph. For example:
```html
<p>My cat is <strong>very</strong> grumpy.</p>
```

## Empty elements
Certain elements don't have content. For example the `<img>` element:
```html
<img src="images/firefox-icon.png" alt="My test image">
```

## HTML Documents
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```

### `<!DOCTYPE html>`
Used to be important for error checking, however does not do very much anymore. It is important to include since sometimes it is required to parse the HTML. Including it just ensures the document behaves correctly.

### `<html></html>`
The `<html>` element, also known as the **root** element, wraps all the content on the entire page.

### `<head></head>`
All the content you want on your page that you don't want to show to users. This includes keywords, page description, CSS styling, character set declarations, etc.

### `<meta charset="utf-8">`
The character set your document will use. You likely will always set it to UTF-8 since it encompasses most written languages.

### `<title></title>`
Sets the title of the page, which appears on the browser tab when the page is loaded.

### `<body></body>`
The `<body>` element encompasses all the content that you want to show users when they visit your page.

## Practice problems
[W3 Schools](https://www.w3schools.com/html/html_exercises.asp)
[Land of Code](http://www.landofcode.com/html-exercises/)

----
Reference: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics
