>"Hypertext" refers to links that connect web pages to one another, either within a single website or between websites.

>HTML uses "markup" to annotate text, images, and other content for display in a Web browser. HTML markup includes special "elements" such as head, title,  and many others.

>The name of an element inside a tag is case-insensitive

>HTML is a markup language that defines the structure of your content.

>Anatomy of an HTML element

 - The opening tag: This consists of the name of the element (in this case, p), wrapped in opening and closing angle brackets. This states where the element begins or starts to take effect — in this case where the paragraph begins.

 - The closing tag: This is the same as the opening tag, except that it includes a forward slash before the element name. This states where the element ends — in this case where the paragraph ends. Failing to add a closing tag is one of the standard beginner errors and can lead to strange results.

 - The content: This is the content of the element, which in this case, is just text.

 - The element: The opening tag, the closing tag, and the content together comprise the element.

 - Attributes contain extra information about the element that you don't want to appear in the actual content.

>Some elements have no content and are called void elements. img tag

>Anatomy of an HTML document

```javascript 
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image" />
  </body>
</html>
```

- \<!DOCTYPE html> — doctype. It is a required preamble. In the mists of time, when HTML was young (around 1991/92), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML, which could mean automatic error checking and other useful things. However, these days, they don't do much and are basically just needed to make sure your document behaves correctly. That's all you need to know for now.

- \<html>\</html> — the \<html> element. This element wraps all the content on the entire page and is sometimes known as the root element. It also includes the lang attribute, setting the primary language of the document.