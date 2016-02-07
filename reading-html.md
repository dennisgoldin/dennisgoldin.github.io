## Universal Attributes

These attributes are common to all `<html>` tags

* `class` -- Is a space-separated list of the classes of the element. Classes allows CSS and JavaScript to select and access specific elements via the class selectors or functions like the method `Document.getElementsByClassName()`.
* `id` -- Defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking (using a fragment identifier), scripting, or styling (with CSS).
* `style` -- Contains CSS styling declarations to be applied to the element. Note that it is recommended for styles to be defined in a separate file or files. This attribute and the [`<style>`](#style) element have mainly the purpose of allowing for quick styling, for example for testing purposes.


## `<!DOCTYPE html>`

This informs the browser which version of HTML (or XML) you used to write the document. Doctype is a declaration, not a tag; you can also refer to it as "document type declaration", or "DTD" for short.


## `<!-- -->`

Comments are textual notations within markup; Comments are usually only readable in the source code view. Comments are represented in HTML and XML as content between '<!--' and '-->'. In XML, the character sequence '--' cannot be used within a comment.

* _parents_: Anything
* _content_: Text

## `<html>`

the main enchilada, the whole `document`, that which wraps all the others... except for [`<!DOCTYPE>`](#doctype), for some reason.

* _parents_: none, it's the top
* _content_: only [`<head>`](#head) and [`<body>`](#body)
* _display_: `block`

### Attributes

* `manifest` -- **DEPRECATED** -- URI of a resource manifest indicating resources that should be cached locally.
* `versin` -- **DEPRECATED** -- Version of the HTML Document Type Definition that governs the current document
* `xmlns` -- Specifies the XML Namespace of the document.  Optional for HTML, required for XHTML.


## `<div>`

A generic page division that should only be used if no other, more semantic choice is appropriate.

* _parents_: anything that accepts [Flow Content][1], which is apparently a lot of things.
* _content_: any [Flow Content][1], palpable content
* _display_: `block`

### Attributes

  * None.

## `<head>`

A container for general information (metadata) about the document including its title and links to definitions of scripts and style sheets.

* _parents_: [`<html>`](#html) element, as its first child.
* _content_: One or more metadata elements [`<metadata>`](#metadata) or [`<link>`](#link) and one [`<title>`](#title)
* _display_: `block`

### Attributes

* `profile` -- **DEPRECATED** -- URIs of one or more metadata profiles, separated by white space.


## `<body>`

Contains the content of an HTML document. There can be only one <body> element in a document.

* _parents_: anything that accepts [Flow Content][1], which is apparently a lot of things.
* _content_: any [Flow Content][1], palpable content
* _display_: `block`

### Attributes

* `alink` -- **DEPRECATED** -- Color of text for hyperlinks when selected. This method is non-conforming, use CSS color property in conjunction with the :active pseudo-class instead.
* `background` -- **DEPRECATED** -- URI of a image to use as a background. This method is non-conforming, use CSS background property on the element instead.
* `bgcolor` -- **DEPRECATED** -- Background color for the document. This method is non-conforming, use CSS background-color property on the element instead.
* `bottommargin` -- **DEPRECATED** -- The margin of the bottom of the body. This method is non-conforming, use CSS margin-bottom property on the element instead.
* `leftmargin` -- **DEPRECATED** -- The margin of the left of the body. This method is non-conforming, use CSS margin-left property on the element instead.
* `link` -- **DEPRECATED** -- Color of text for unvisited hypertext links. This method is non-conforming, use CSS color property in conjunction with the :link pseudo-class instead.
* `onafterprint` -- Function to call after the user has printed the document.
* `onbeforeprint` -- Function to call when the user requests printing of the document.
* `onbeforeunload` -- Function to call when the document is about to be unloaded.
* `onblur` -- Function to call when the document loses focus.
* `onerror` -- Function to call when the document fails to load properly.
* `onfocus` -- Function to call when the document receives focus.
* `onhashchange` -- Function to call when the fragment identifier part (starting with the hash ('#') character) of the document's current address has changed.
* `onlanguagechange` -- Function to call when the preferred languages changed.
* `onload` -- Function to call when the document has finished loading.
* `onmessage` -- Function to call when the document has received a message.
* `onoffline` -- Function to call when network communication has failed.
* `ononline` -- Function to call when network communication has been restored.
* `onpopstate` -- Function to call when the user has navigated session history.
* `onredo` -- Function to call when the user has moved forward in undo transaction history.
* `onresize` -- Function to call when the document has been resized.
* `onstorage` -- Function to call when the storage area has changed.
* `onundo` --Function to call when the user has moved backward in undo transaction history.
* `onunload` -- Function to call when the document is going away.
* `rightmargin` -- **DEPRECATED** -- The margin of the right of the body. This method is non-conforming, use CSS margin-right property on the element instead.
* `text` -- **DEPRECATED** -- Foreground color of text. This method is non-conforming, use CSS color property on the element instead.
* `topmargin` -- **DEPRECATED** -- The margin of the top of the body. This method is non-conforming, use CSS margin-top property on the element instead.
* `vlink` -- **DEPRECATED** -- Color of text for visited hypertext links. This method is non-conforming, use CSS color property in conjunction with the :visited pseudo-class instead.


## `<img>`

This tag inserts an image in the document. Must have a start tag and must not have an end tag.

* _parents_: [`<html>`](#html) element, as its first child.
* _content_: 	[Flow content][1], [phrasing content][2], embedded content, palpable content. If the element has a usemap attribute, it also is a part of the interactive content category. It is an empty element.
* _display_: `block`

### Attributes

* `align` -- **DEPRECATED** since HTML4.01, **OBSOLETE** since HTML5 -- Use the [vertical-align][3] CSS property.  The alignment of the image with respect to its surrounding context.
* `alt` -- This attribute defines the alternative text describing the image. Users will see this displayed if the image URL is wrong, the image is not in one of the supported formats, or if the image is not yet downloaded.
Usage note: Omitting this attribute indicates that the image is a key part of the content, but no textual equivalent is available. Setting this attribute to the empty string indicates that this image is not a key part of the content; non-visual browsers may omit it from rendering.
* `border` -- **DEPRECATED** since HTML4.01, **OBSOLETE** since HTML5 -- The width of a border around the image.
* `crossorigin` -- This enumerated attribute indicates if the fetching of the related image must be done using CORS or not. [CORS-enabled images][4] can be reused in the <canvas> element without being tainted. The allowed values are:
  * `anonymous` -- A cross-origin request (i.e., with Origin: HTTP header) is performed. But no credential is sent (i.e., no cookie, no X.509 certificate, and no HTTP Basic authentication is sent). If the server does not give credentials to the origin site (by not setting the Access-Control-Allow-Origin: HTTP header), the image will be tainted and its usage restricted.
  * `use-credentials` -- A cross-origin request (i.e., with Origin: HTTP header) performed with credential is sent (i.e., a cookie, a certificate, and HTTP Basic authentication is performed). If the server does not give credentials to the origin site (through Access-Control-Allow-Credentials: HTTP header), the image will be tainted and its usage restricted.
When not present, the resource is fetched without a CORS request (i.e., without sending the Origin: HTTP header), preventing its non-tainted usage in <canvas> elements. If invalid, it is handled as if the enumerated keyword anonymous was used. See [CORS settings attributes][5] for additional information.
* `height` -- The intrinsic height of the image in HTML5 CSS pixels, or HTML 4 in pixels or as a percentage.
* `hspace` -- **DEPRECATED** since HTML4.01, **OBSOLETE** since HTML5 -- The number of pixels of white space to insert to the left and right of the image.
* `ismap` -- This Boolean attribute indicates that the image is part of a server-side map. If so, the precise coordinates of a click are sent to the server. This attribute is allowed only if the [`<img>`](#img) element is a descendant of an <a> element with a valid href attribute.
* `longdesc` -- The URL of a description of the image to be displayed, which supplements the alt text.
* `name` -- **DEPRECATED** since HTML4.01, **OBSOLETE** since HTML5 -- A name for the element. It is supported in HTML 4 only for backward compatibility. Use the id attribute instead.
* `sizes` -- A list of one or more strings separated by commas indicating a set of source sizes. Each source size consists of:
  1. A media condition. This must be omitted for the last item.
  2. a source size value.
Source size values specify the intended display size of the image. User agents use the current source size to select one of the sources supplied by the `srcset` attribute, when those sources are described using width ('w') descriptors. The selected source size affects the intrinsic size of the image (the image’s display size if no CSS styling is applied). If the `srcset` attribute is absent, or contains no values with a width (w) descriptor, then the sizes attribute has no effect.
* `src` -- The image URL. This attribute is mandatory for the [`<img>`](#img) element. On browsers supporting `srcset`, src is treated like a candidate image with a pixel density descriptor 1x unless an image with this pixel density descriptor is already defined in `srcset` or `srcset` contains 'w' descriptors.
* `srcset` -- A list of one or more strings separated by commas indicating a set of possible image sources for the user agent to use. Each string is composed of:
  1. a URL to an image,
  2. optionally, whitespace followed by one of:
    * a width descriptor, that is a positive integer directly followed by 'w'. The width descriptor is divided by the source size given in the sizes attribute to calculate the effective pixel density.
    * a pixel density descriptor, which is a positive floating point number directly followed by 'x'.
If no descriptor is specified, the source is assigned the default descriptor: 1x.

It is invalid to mix width descriptors and pixel density descriptors in the same `srcset` attribute. Duplicate descriptors (for instance, two sources in the same `srcset` which are both described with '2x') are invalid, too.

User agents are given discretion to choose any one of the available sources. This provides them with significant leeway to tailor their selection based on things like user preferences or bandwidth conditions.
* `width` -- The intrinsic width of the image in HTML5 CSS pixels, or HTML 4 in pixels or as a percentage.
* `usemap` -- The partial URL (starting with '#') of an image map associated with the element.
Usage note: You cannot use this attribute if the [`<img>`](#img) element is a descendant of an <a> or <button> element.
* `vspace` --  **DEPRECATED** since HTML4.01, **OBSOLETE** since HTML5 -- The number of pixels of white space to insert above and below the image.


## `<ul>`

A list of unordered items and their order in the list is meaningless. Typically, unordered-list items are displayed with a bullet, which can be of several forms, like a dot, a circle or a squared. The bullet style is not defined in the HTML description of the page, but in its associated CSS, using the [list-style-type property][6]. There is no limitation to the depth and imbrication of lists defined with the [`<ol>`](#ul) and [`<ul>`](#ul) elements.

* _parents_: anything that accepts [Flow Content][1], which is apparently a lot of things.
* _content_: any [Flow Content][1], zero or more [`<li>`](#li) elements, eventually mixed with [`<ol>`](#ol) and [`<ul>`](#ul) elements
* _display_: `block`

### Attributes

* `compact` -- **DEPRECATED** use the CSS [list-style-type property][6] instead -- This Boolean attribute hints that the list should be rendered in a compact style. The interpretation of this attribute depends on the user agent and it doesn't work in all browsers. The [`<ul>`](#ul) element should be styled using CSS. To give a similar effect as the compact attribute, the CSS property line-height can be used with a value of 80%.
* `type` -- Used to set the bullet style for the list. The values defined under HTML3.2 and the transitional version of HTML 4.0/4.01 are:
  * circle
  * disc
  * square
A fourth bullet type has been defined in the WebTV interface, but not all browsers support it: triangle.

If not present and if no CSS [list-style-type property][6] does apply to the element, the user agent decide to use a kind of bullets depending on the nesting level of the list.


## `<li>`

The List Item Element is used to represent an item in a list.  In menus and unordered lists, list items are usually displayed using bullet points. In ordered lists, they are usually displayed with an ascending counter on the left, such as a number or letter.

* _parents_: an ordered list [`<ol>`](#ol), an unordered list [`<ul>`](#ul), or a menu [`<menu>`](#menu)
* _content_: any [Flow Content][1], mixed with [`<ol>`](#ol) and [`<ul>`](#ul) elements
* _display_: `block`

### Attributes

* `value` -- integer attribute indicates the current ordinal value of the list item for the [`<ol>`](#ol) element. The only allowed value for this attribute is a number, even if the list is displayed with Roman numerals or letters. List items that follow this one continue numbering from the value set. The value attribute has no meaning for unordered lists [`<ul>`](#ul) or for menus [`<menu>`](#menu). This attribute was deprecated in HTML4, but reintroduced in HTML5. Prior to Gecko 9.0, negative values were incorrectly converted to 0. Starting in Gecko 9.0 all integer values are correctly parsed.
* `type` -- **DEPRECATED** use the CSS [list-style-type property][6] instead -- This character attribute indicates the numbering type:
  * a: lowercase letters
  * A: uppercase letters
  * i: lowercase Roman numerals
  * I: uppercase Roman numerals
  * 1: numbers
This type overrides the one used by its parent <ol> element, if any.


## `<span>`

The HTML [`<span>`](#span) element is a generic inline container for phrasing content, which does not inherently represent anything. It can be used to group elements for styling purposes (using the class or id attributes), or because they share attribute values, such as lang. It should be used only when no other semantic element is appropriate. <span> is very much like a <div> element, but <div> is a block-level element whereas a <span> is an inline element.

* _parents_: any element taking [Flow Content][1] or [Phrasing Content][7]
* _content_: any [Flow Content][1], [Phrasing Content][7]
* _display_: `inline`

### Attributes

  * None.


###### Footnotes

[1]<https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories#Flow_content>

[2]<https://developer.mozilla.org/en-US/docs/HTML/Content_categories#Phrasing_content>

[3]<https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align>

[4]<https://developer.mozilla.org/en-US/docs/CORS_Enabled_Image>

[5]<https://developer.mozilla.org/en-US/docs/HTML/CORS_settings_attributes>

[6]<https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type>

[7]<https://developer.mozilla.org/en-US/docs/HTML/Content_categories#Phrasing_content>
