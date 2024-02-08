looking at some elements that allow you to embed a wide variety of content types into your webpages: the \<iframe>, \<embed> and \<object> elements. \<iframe>s are for embedding other web pages, and the other two allow you to embed external resources such as PDF files.

```html
<iframe
    src="https://developer.mozilla.org/en-US/docs/Glossary"
    width="100%"
    height="500"
    allowfullscreen
    sandbox>
    <p>
      <a href="/en-US/docs/Glossary">
        Fallback link for browsers that don't support iframes
      </a>
    </p>
  </iframe>
```
If you have a look at your browser's console, you'll see an error message like the following:

>chromewebdata/:1 Refused to display 'https://developer.mozilla.org/' in a frame because it set 'X-Frame-Options' to 'deny'.

border: none
If used, the \<iframe> is displayed without a surrounding border. Otherwise, by default, browsers display the \<iframe> with a surrounding border (which is generally undesirable).

allowfullscreen
If set, the \<iframe> is able to be placed in fullscreen mode using the Fullscreen API (somewhat beyond the scope of this article.)

src
This attribute, as with \<video> /  \<img>, contains a path pointing to the URL of the document to be embedded.

width and height
These attributes specify the width and height you want the iframe to be.

sandbox
This attribute, which works in slightly more modern browsers than the rest of the \<iframe> features (e.g. IE 10 and above) requests heightened security settings; we'll say more about this in the next section.


```html 
<object data="mypdf.pdf" type="application/pdf" width="800" height="1200">
  <p>
    You don't have a PDF plugin, but you can
    <a href="mypdf.pdf">download the PDF file. </a>
  </p>
</object>
```
|   |\<embed>|\<object>|
|---|-------|--------|
|URL of the embedded content|src|data|
|accurate media type of the embedded content|type|type
|height and width (in CSS pixels) of the box controlled by the plugin|height width|height width
|names and values, to feed the plugin as parameters	|ad hoc attributes with those names and values|single-tag \<param> elements, contained within \<object>
|independent HTML content as fallback for an unavailable resource|not supported (\<noembed> is obsolete)|contained within \<object>, after \<param> elements