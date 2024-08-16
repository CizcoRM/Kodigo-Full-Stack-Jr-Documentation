# HTML Basics

## **What is HTML?**

HTML (HyperText Markup Language) is the standard language used to create and design documents on the World Wide Web. **HTML uses a system of tags and attributes** to define different parts of the document, making it possible to format and display content in a structured and visually appealing way.

---

- **Basic structure of an HTML tag**
`<tag attribute="value"> content </tag>`
- **Tags:** In HTML5 there's a specific set of predefined tags, these are enclosed within opening `<tag>` and closing tags `</tag>` .
- **Attributes** determine specific information about the tag. The value is always enclosed in **double quotes**.

    `<tag attribute="value"> content </tag>`

    There are 3 types of attributes:

    1. **Set of values**: These only allow specific values. Any other value will be invalid.
    2. **Free values**: These are attributes where you can freely specify a value, such as a URL or text.
    3. **Boolean values**: These are attributes that must have either a true or false value.
- **Tag content:** This is where you place the information you want to be affected by the tag.

    `<tag id="data" class="class1" lang="es">Content</tag>`

    A tag can have multiple attribute-value pairs. However, the same attribute should never be repeated within a single tag.

- **Commentary** ignored by the browser, used to explain and document the code.

    `<!-- This is a commentary -->`

## **- Common Attributes**

| Attribute | Value | Description |
| --- | --- | --- |
| id | name | Sets a unique identifier for the tag can only be used once per document. `<div id="unique-identifier">This is a div with an id</div>` |
| class | name | Sets a class for an HTML tag. It can be repeated throughout the document. `<p class="highlight important">This is a paragraph with classes</p>` |
| style | CSS styles | Applies CSS properties directly to the specific HTML element. `<span style="color: blue; font-weight: bold;">This is a span with inline style</span>` |

### Identifier: The id attribute

This is an identifier for an HTML tag and a way to give it a name.

- It must not start with a number, but can contain numbers later on.
- The text should be in `kebab-case`
- Without strange characters, accents, or emojis.
- There cannot be two elements with the same `id`.

`<div id="unique-identifier">This is a div with an id</div>`

They are used when we want to locate specific areas that we know will not be repeated on the same page. Unless it's necessary to identify a unique area on the page, it's best to avoid using `id`.

### Classes: The class attribute

There can be elements with the same class in a document and a tag can have multiple different classes separated by space, not necessarily a single one.

`<p class="highlight important">This is a paragraph with classes</p>`

### Inline Styles: The style attribute

It is used in HTML tags to embed CSS code directly in the tag itself. However, in most cases, it is not recommended to add the styles in this way but to place the CSS code in a separate `.css` document of our HTML document.

`<span style="color: blue; font-weight: bold;">This is a span with inline style</span>`

## **- Basic HTML structure**

The document structure is divided into **three parts.** **Document type `<**!DOCTYPE html>`. Then, we open the **`<html>`** tag that will contain two main parts: the document **header** **`<head>`** and the document **body** **`<body>`**.

``` HTML
<!DOCTYPE html>
<html lang="es">
 <head>
   <title>Títule</title>
   <meta charset="utf8">
 </head>
 <body>
   ...
 </body>
</html>
```

`<!DOCTYPE html>`  It must always be specified so that the browser knows what type of HTML document it is.

**`<head>`** is not a visual part of the web page, but a part of where certain metadata tags are included for good SEO.

**`<body>`** All the visual elements of a page are located inside the tag.

### **- Other Attributes**

| Metadata Attribute | Value | Description |
| --- | --- | --- |
| title  | message | Message displayed in a tooltip when moving the mouse over an element. `<p title="This is a tooltip">Hover over me to see the title tooltip</p>` |
| data-* | text | Metadata in the tag itself. Any name with data- para prefix containing information, usually oriented to be used from Javascript or CSS, can be used.. `<div data-user-id="123" data-role="admin">Custom data attributes</div>` |
| accesskey | shortcut | Key combination that can be pressed by the user to activate the element.`<a href="#" accesskey="h">Home (Press Alt + h)</a>` |
| lang | language | Indicates the language of the HTML tag content.`<p lang="es">Hola, ¿cómo estás?</p>` |
| translate | yes / no | Sets the directionality of the text. `<p translate="no">Do not translate this text</p>` |
| dir | ltr / rtl | Establece la direccionalidad del texto (left to right o right to left).`<p dir="rtl">This text will be right-to-left</p>` |

### - Obsolete Tags

| Obsolete Tag | Description | Alternative |
| --- | --- | --- |
| `<applet>` | Tag for Java applets. | Javascript, DOM and CSS |
| `<acronym>` | Indicates an acronym. | `<abbr>` |
| `<bgsound>` | Specifies a background sound. | `<audio>` |
| `<dir>` | Indicates a list of files or folders. | `<ul>` |
| `<frame>` | Defines a specific frame. | `<iframe>`  |
| `<isindex>` | Field to search in the document. | `<input>` |
| `<listing>`, `<xmp>` | Source code fragments. | `<pre>`,`<code>` |
| `<noembed>` | Alternative (fallback) for content. | `<object>`  |
| `<strike>` | Displays strikethrough text. | `<s>` |
|  `<basefont>` | Defines a default font. | CSS: font-family |
| `<big>` | Increases text size. | CSS: font-size |
| `<blink>` | Displays blinking text. | CSS: animation |
| `<center>` | Centers the text. | CSS: text-align |
| `<font>` | Changes the font or its characteristics. | CSS: font-family |
| `<marquee>` | Displays text moving from side to side. | CSS: animation |
| `<multicol>` | Multiple columns. | CSS: columns |
| `<nobr>` | Prevents text from line breaking. | CSS: white-space |
| `<spacer>` | Inserts a horizontal space. |   |
| `<tt>` | Displays text with a monospaced font. | `<code>` |

### TAGS

### - `<head>` Document Header tags

There are several tags that can be used in the `<head>` section of the HTML document.

| HTML Tag | Where can it be used? | Description |
|----------|------------------------|-------------|
| `<title>` | ✅ `<head>` ❌ `<body>` | Indicates the title of the page (browser tab or title in Google search results). |
| `<base>` | ✅ `<head>` ❌ `<body>` | Base URL for links (used to manage relative paths). |
| `<link>` | ✅ `<head>` ❌ `<body>` | Establishes a relationship between the current document and an external one. See link tag |
| `<meta>` | ✅ `<head>` ❌ `<body>` | Sets a specific metadata in the current document. See meta tag |
| `<style>` | ✅ `<head>` ✅ `<body>` | Creates CSS styles that will only affect the current document. |
| `<script>` | ✅ `<head>` ✅ `<body>` | Indicates a script to load or execute on the current page. |
