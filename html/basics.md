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

Reference: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics
