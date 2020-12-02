# CSS Basics

## What is CSS?

CSS is known as a **syle sheet language**, which just means it's a computer language that alters the presentation of structured documents, like HTML and markdown.

## CSS Syntax

![Anatomy of a CSS ruleset](css-declaration-small.png)

This object is called a **ruleset** or **rule**. Here is the breakdown:

### Selector
The HTML element name to be styled by the rule. In this case, anything with a `p` tag in the HTML that is being styled will turn red.

### Declaration
A single rule that describes the properties to style. There can be multiple rules within the ruleset.

### Property
These are the ways you can style an HTML element. There are a lot of properties in CSS and it can feel overwhelming! In this [reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference), you can find a list of CSS properties and find the valid property values.

### Property value
This sets the value for a given property. In the example above, it sets `color` to `red`, but it could easily be `blue`, `green`, `#6a0dad`, etc.

You can modify multiple properties in a single ruleset:
```css
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

And you can modify multiple elements in a single ruleset:
```css
p, li, h1 {
  color: red;
}
```

## Types of selectors
We've been using HTML classes as selectors, but for greater flexibility we can use other identifiers to modify our HTML.

### Element selector
What we've been talking about so far, the HTML element to be modified. I.e. `p`, `li`, `h1`, etc.

### ID selector
An ID selector starts with a `#`. A unique that you define to associate with various elements. For example, your rule set could look like:
```css
#test-id {
  color: red;
}
```
And if you had HTML elements like `<p id="test-id">` and `<p id="example-id">`, it would turn only the <p> with the id `test-id` red. An ID can only be used once in your HTML.

### Class selector
A class selector starts with a `.`. This selects HTML elements based on their class. This is similar to the id selector, however a class can apply to multiple elements. For example, your rule set could look like:
```css
.test-class {
  color: red;
}
```
And if you had HTML elements like `<p class="test-id">` or `<h1 class="test-id">`, it would turn that paragraph and header red.

### Attribute selector
This selects elements on the page with a specified attribute. For example:
```css
a[href="http://google.com"] {
  color: red;
}
```
This would change only a link referencing google.com to the color red, but a link to any other site would remain blue.

### Pseudo-class selector
This selects the specified element but only when in a specified state. For example:
```css
a:hover {
  color: red;
}
```
Makes `<a>` red, but only when the mouse is hovering over the link.

Read more on selectors [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors).

## Box Model

CSS is based on the box model, with each box on your page having `padding`, `border`, andd `margin`.

![Box model example](box-model.png)

You can alter these boxes using various properties such as `width`, `background-color` (the color behind an element's content and padding), `color` (the color of an elements content - usually text), `text-shadow` (the drop shadow on the text inside an element), `display` (the display mode of an element).


Reference: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics

# Diving Deeper

## Preprocessors
All of this might seem reasonable for a basic website, but with websites getting more and more complex, it's getting more challenging to write CSS. There are several tools that make it easier to write dynamic styles. One of these tools is called [Sass](https://sass-lang.com/guide). It is a preprocesser which means that it converts `.scss` files (sassy css), and converts them to normal CSS files that the browser understands. The linked guide has great examples of scss to css conversions.

## Media queries
With the prevelance of phones, it's important to style your site in a way that looks good on all devices. It would be exhausting to rewrite your CSS for each different device you encounter, so [media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries) are great to apply conditional logic to your CSS to ensure your styles look good on any screen.

# Practice Problems
- [W3 Schools](https://www.w3schools.com/css/css_exercises.asp) (Note that this site makes you write CSS in an HTML file, which is an alternative to writing it in a `.css` file)
