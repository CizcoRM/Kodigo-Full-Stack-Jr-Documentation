**What is HTML?**

HTML (HyperText Markup Language) is the standard language used to create and design documents on the World Wide Web. **HTML uses a system of tags and attributes** to define different parts of the document, making it possible to format and display content in a structured and visually appealing way.

---

- **Basic estructure of a HTML tag**
`<tag attribute="value"> content </tag>`
- **Tags:** In HTML5 there's a specific set of predefined tags, these are enclosed within opening `<tag>` and closing tags `</tag>` .
- **Attributes** determine specific information about the tag. The value is always enclosed in **double quotes**.
    
    `<tag attribute="value"> content </tag>`
    
    There are 3 types of attributes:
    
    1. **Set of values**: These only allow specific values. Any other value will be invalid.
    2. **Free values**: These are attributes where you can freely specify a value, such as a URL or text.
    3. **Boolean values**: These are attributes that must have either a true or false value.
- **Tag content:** This is where you place the information you want to be affected by the tag.
    
    `<tag id="data" class="class1" lang="es">Content</TAG>`
    
    A tag can have multiple attribute-value pairs. However, the same attribute should never be repeated within a single tag.
    
- **Commentary** ignores by we browser, used to explain and document the code.
    
    `<!-- This is a commentaty -->`
    

**Common Attributes**

| Attribute | Value | Description |
| --- | --- | --- |
| id | name | Sets a unique identifier for the tag can only be used once per document.
<div id="unique-identifier">This is a div with an id</div> |
| class | name | Sets a class for an HTML tag. It can be repeated throughout the document.
<p class="highlight important">This is a paragraph with classes</p> |
| style | CSS styles | Applies CSS properties directly to the specific HTML element.
<span style="color: blue; font-weight: bold;">This is a span with inline style</span> |

**Identifier: The id attribute**

This is an identifier for an HTML tag and a way to give it a name.

- It must not start with a number, but can contain numbers later on.
- The text should be in **`kebab-case`**
- Without strange characters, accents, or emojis.
- There cannot be two elements with the same **`id`**.

```html
<div id="unique-identifier">This is a div with an id</div>
```

They are used when we want to locate specific areas that **we know will not be repeated on the same page**. Unless it's necessary to identify a unique area on the page, it's best to avoid using **`id`**.

**Classes: The class attribute**

There can be elements with the same class in a document and a tag can have multiple different classes separated by space, not necessarily a single one.

```html
<p class="highlight important">This is a paragraph with classes</p>
```

**Inline Styles: The style attribute**

It is used in HTML tags to embed CSS code directly in the tag itself. However, in most cases, it is not recommended to add the styles in this way but to place the CSS code in a separate **`.css`** document of our HTML document.

```html
<span style="color: blue; font-weight: bold;">This is a span with inline style</span>
```

**Basic HTML structure**

The document structure is divided into **three parts.** **Document type `<**!DOCTYPE html>`. Then, we open the **`<html>`** tag that will contain two main parts: the document **header** **`<head>`** and the document **body** **`<body>`**.

```
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

**`<**!DOCTYPE html>`  It must always be specified so that the browser knows what type of HTML document it is.

**`<head>`** is not a visual part of the web page, but a part of where certain metadata tags are included for good SEO.

**`<body>`** All the visual elements of a page are located inside the tag.

Other Attributes

| Metadata Attribute | Value | Description |
| --- | --- | --- |
| title | mensaje | Mensaje mostrado en un tooltip al mover el ratón encima sobre un elemento.
<p title="This is a tooltip">Hover over me to see the title tooltip</p> |
| data-* | texto | Metadatos en la propia etiqueta. Se puede usar cualquier nombre con prefijo data-para  que contenga información, habitualmente orientada a utilizarse desde Javascript o CSS.
<div data-user-id="123" data-role="admin">Custom data attributes</div> |
| accesskey | atajo | Combinación de teclas que puede pulsar el usuario para activar el elemento.
<a href="#" accesskey="h">Home (Press Alt + h)</a> |
| Language attributes | Value | Description |
| lang | idioma | Indica el idioma del contenido de la etiqueta HTML.
<p lang="es">Hola, ¿cómo estás?</p> |
| translate | yes | no | Indica si el contenido de la etiqueta se debería traducir o no.
<p translate="no">Do not translate this text</p> |
| Other attributes | Value | Description |
| dir | ltr | rtl | Establece la direccionalidad del texto (left to right o right to left).
<p dir="rtl">This text will be right-to-left</p> |

| Etiqueta obsoleta | Descripción | Alternativa |
| --- | --- | --- |
| <applet> | Etiqueta para applets Java. | Javascript, DOM y CSS |
| <acronym> | Indica un acrónimo. | <abbr> |
| <bgsound> | Especifica un sonido de fondo. | <audio> |
| <dir> | Indica una lista de archivos o carpetas. | <ul> |
| <frame> | Define un marco específico. | <iframe> |
| <frameset> | Define un conjunto de marcos. | ⤴ |
| <noframes> | Indica una alternativa si el navegador no soporta marcos. | ⤴ |
| <isindex> | Campo para búscar en el documento. | <input> |
| <listing>, <xmp> | Fragmentos de código fuente. | <pre><code> |
| <noembed> | Alternativa (fallback) para contenidos. | <object> |
| <strike> | Muestra un texto tachado. | <s> |
| <basefont> | Define una tipografía por defecto. | https://lenguajecss.com/css/fuentes-y-tipografias/tipografias/ |
| <big> | Aumenta el tamaño del texto. | https://lenguajecss.com/css/fuentes-y-tipografias/tipografias/ |
| <blink> | Muestra el texto de forma parpadeante. | https://lenguajecss.com/css/animaciones/animaciones/ |
| <center> | Centra el texto. | https://lenguajecss.com/css/fuentes-y-tipografias/textos-y-alineaciones/ |
| <font> | Cambia la tipografía o sus características. | https://lenguajecss.com/css/fuentes-y-tipografias/tipografias/ |
| <marquee> | Muestra el texto moviéndose de un lado a otro. | https://lenguajecss.com/css/animaciones/animaciones/ |
| <multicol> | Columnas múltiples. | https://lenguajecss.com/css/maquetacion-y-colocacion/multi-column/ |
| <nobr> | Evita que un texto haga un salto de línea. | https://lenguajecss.com/css/fuentes-y-tipografias/textos-y-alineaciones/ |
| <spacer> | Inserta un espacio horizontal. | &nbsp; |
| <tt> | Muestra el texto con una fuente monoespaciada. | <code> |