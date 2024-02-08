# html head

The HTML head is the contents of the \<head> element.

```html
<head>
  <meta charset="utf-8" />
  <title>My test page</title>
</head>
```

## title

\<title> is used for title of the page and also uses in saving bookmarks

## metadata 

\<meta> 

` <meta charset="utf-8" /> `

This element specifies the document's character encoding — the character set that the document is permitted to use.

### Adding an author and description

- name specifies the type of meta element it is; what type of information it contains.
- content specifies the actual meta content.

``` html
<meta name="author" content="Chris Mills" />
<meta
  name="description"
  content="The MDN Web Docs Learning Area aims to provide complete beginners to the Web with all they need to know to get started with developing websites and applications." />
  <meta name="keywords" content="fill, in, your, keywords, here">
```

## Adding custom icons to your site

A favicon can be added to your page by:

1. Saving it in the same directory as the site's index page, saved in .ico format (most also support favicons in more common formats like .gif or .png)

2. Adding the following line into your HTML's \<head> block to reference it:

` <link rel="icon" href="favicon.ico" type="image/x-icon" /> `

There are lots of other icon types to consider these days as well. For example, you'll find this in the source code of the MDN Web Docs homepage:

```html
<!-- third-generation iPad with high-resolution Retina display: -->
<link
  rel="apple-touch-icon"
  sizes="144x144"
  href="https://developer.mozilla.org/static/img/favicon144.png" />
<!-- iPhone with high-resolution Retina display: -->
<link
  rel="apple-touch-icon"
  sizes="114x114"
  href="https://developer.mozilla.org/static/img/favicon114.png" />
<!-- first- and second-generation iPad: -->
<link
  rel="apple-touch-icon"
  sizes="72x72"
  href="https://developer.mozilla.org/static/img/favicon72.png" />
<!-- non-Retina iPhone, iPod Touch, and Android 2.1+ devices: -->
<link
  rel="apple-touch-icon"
  href="https://developer.mozilla.org/static/img/favicon57.png" />
<!-- basic favicon -->
<link
  rel="icon"
  href="https://developer.mozilla.org/static/img/favicon32.png" />
```

- The \<link> element should always go inside the head of your document. This takes two attributes, rel="stylesheet", which indicates that it is the document's stylesheet, and href, which contains the path to the stylesheet file:

`<link rel="stylesheet" href="my-css-file.css" />`

- The \<script> element should also go into the head, and should include a src attribute containing the path to the JavaScript you want to load, and defer, which basically instructs the browser to load the JavaScript after the page has finished parsing the HTML. This is useful as it makes sure that the HTML is all loaded before the JavaScript runs, so that you don't get errors resulting from JavaScript trying to access an HTML element that doesn't exist on the page yet. 

`<script src="my-js-file.js" defer></script>`

## Setting the primary language of the document

This can be done by adding the lang attribute to the opening HTML tag

`<html lang="en-US"></html>`

You can also set subsections of your document to be recognized as different languages. For example

`<p>Japanese example: <span lang="ja">ご飯が熱い。</span>.</p>`