# Language-Docs-Review
Reveiw Important Point in programming language



1. What is the different between width:auto and width: 100%?
- Width 100% : It will make content width 100%. margin, border, padding will be added to this width and element will overflow if any of these added.
- Width auto : It will fit the element in available space including margin, border and padding. space remaining after adjusting margin + padding + border will be available width/ height.
- Width 100% + box-sizing: border box : It will also fits the element in available space including border, padding (margin will make it overflow the container).
2. What is the different between attribute and propeerties in HTML:5
- Attributes are additional information which we can put in the HTML to initialize certain DOM properties.
- Properties are formed when the browser parses the HTML and generates the DOM. Each of the elements in the DOM have their own set of properties which are all set by the browser.
- When writing HTML source code, you can define attributes on your HTML elements. Then, once the browser parses your code, a corresponding DOM node will be created. This node is an object, and therefore it has properties.
- For instance, this HTML element:
```<input type="text" value="Name:">``` has 2 attributes (type and value).
- Once the browser parses this code, a HTMLInputElement object will be created, and this object will contain dozens of properties like: accept, accessKey, align, alt, attributes, autofocus, baseURI, checked, childElementCount, childNodes, children, classList, className, clientHeight, etc.

3. What is the difference between HTML and XHTML?
- HTML is the standard markup language for creating web pages, while XHTML is a stricter and more standardized version of HTML. Both HTML and XHTML include a wide range of features, such as support for multimedia, styling, and scripting.
