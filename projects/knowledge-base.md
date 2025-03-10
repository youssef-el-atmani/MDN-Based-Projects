# Knowledge Base

> Here I'll store all the knowledge starting from the date `27 Feb 2025`\
> That knowledge is strictly related to `web dev`, and mostly related to `Front End Dev`\
> Also the knowledge that will be listed here is strictly practical, theoretical one will have its own file\

## Structuring Content With HTML

### Basic HTML Syntax

#### HTML tags

Tags in HTML are not case-sensitive. This means they can be written in uppercase or lowercase. For example, a `<title>` tag could be written as `<title>`, `<TITLE>`, `<Title>`, `<TiTlE>`, etc., and it will work. However, it is best practice to write all tags in lowercase for consistency and readability.

> [!IMPORTANT]
> In order to keep that in mind, write at least a single element in that inconsistent-way\
> Prettier will automatically transfer those inconsistent-tags to lowercased version, that's okay, do it anyway even if it will not be saved

#### Boolean Attributes (HTML)

A `boolean attribute` in HTML is an attribute that represents `true` or `false`
values. If an HTML tag contains a boolean attribute — no matter
the value of that attribute — the attribute is set to `true`
on that element. If an HTML tag does not contain the attribute,
the attribute is set to `false`.

> [!IMPORTANT]
> To keep that the `boolean attribute` concept in your mind, write it at least once,\
> Some examples are: `required`, `readonly`, and `disabled`, you can use one of those if you want.

#### Double Quotes

Both single and double quotes are valid, but for consistency stick to `double quotes` whenever you have to choose between them.\
Wrapping HTML attribute values as an example: `class="first-title"`.

> [!IMPORTANT]
> Use only double quotes in your HTML code whenever needed

### Head Elem: Webpage metadata

The head's job is to contain metadata about the document.

> Dictionary: metadata is information that is given to describe or help you use other information

#### title element

The title element are used in `page tab`\
and also as suggestion name when you try to bookmark a webpage

> [!IMPORTANT]
> Include a `title element` in the `head`.

#### `<meta>` elem

##### meta charset utf-8

`<meta charset="utf-8" />`\
This element specifies the document's character encoding.\
`utf-8` is a universal character set that includes pretty much any character from any human language.

> Some browsers (like Chrome) automatically fix incorrect encodings, so depending on what browser you use, you may not see this problem. You should still set an encoding of `utf-8` on your page anyway to avoid any potential problems in other browsers.

> [!IMPORTANT]
> Include `<meta charset="utf-8" />` in your page.

##### meta with name & content attr

- `name` specifies the type of meta element it is; what type of information it contains.
- `content` specifies the actual meta content.\

Two such meta elements that are useful to include on your page define the author of the page, and provide a concise description of the page.

```html
<meta name="author" content="Chris Mills" />
<meta
  name="description"
  content="The MDN Web Docs Learning Area aims to provide
complete beginners to the Web with all they need to know to get
started with developing websites and applications."
/>
```

> This is good for SEO.

> [!IMPORTANT]
> Include a meta element that include your name\
> And another meta element that include description to the page content\
> Do something similar to the example above

#### favicon

You may see (depending on the browser) favicons displayed in the browser tab containing each open page, and next to bookmarked pages in the bookmarks panel.

A favicon can be added to your page by:

- Saving it in the same directory as the site's index page, saved in .ico format (most also support favicons in more common formats like .gif or .png)
- Adding the following line into your HTML's <head> block to reference it:\
  `<link rel="icon" href="favicon.ico" type="image/x-icon" />`

> [!IMPORTANT]
> Add a favicon to your page,\
> The link element should have `rel`, `href`, and `type` attributes.

#### Applying CSS

Applying CSS done through the `link` element,\
The `link` element should go inside the `head` element, and should have:

- `rel` attribute with value: `stylesheet`,
- `href` attribute with the `css file path` as its value.

Here is how it should be: `<link rel="stylesheet" href="my-css-file.css" />`

> [!IMPORTANT]
> Create an empty css file and link it.
> The `link` elem should have `rel` and `href` attributes with there right values

#### Applying JavaScript

Applying JS Done using the `script` element,\
It should go in the `head` elem, and include the following attributes:

- `src` with `js file path` as it value,
- `defer` which is a `boolean attribute` that basically instructs the browser to load the JavaScript `after` the page has finished parsing the HTML

> [!IMPORTANT]
> Create an empty JS file,\
> The `script` elem should go in the `head`, and should include:
>
> - `src`,
> - and `defer` attributes

#### Setting primary language for the document [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Webpage_metadata#setting_the_primary_language_of_the_document)

This can be done by adding the `lang` attribute to the opening HTML tag as: `<html lang="en-US">`

> Your HTML document will be indexed more effectively by search engines if its language is set (allowing it to appear correctly in language-specific results, for example)\
> and it used by screen readers to use the right language

You can also set subsections of your document to be recognized as different languages.

`<p>Arabic Example <span lang="ar">مرحبا</span></p>`

> [!IMPORTANT]
> Add the `lang` attr to the whole document, use `en` for now,
> and use it for some subsection of the document, maybe for `p`, or `span`

### ✅💻 01 Initial

It is a simple project where I put all the above concepts that is mostly related to metadata that goes in the head elem.

- [code](/projects/html-stage/01-initial/)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/01-initial/index.html)

### Heading & paragraphs in HTML [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Headings_and_paragraphs)

Structured content makes the reading experience easier and more enjoyable.

#### paragraphs

In HTML, each paragraph has to be wrapped in a `<p>` element.

#### headings

There are six heading elements: `h1`, `h2`, `h3`, `h4`, `h5`, and `h6`. Each element represents a different level of content in the document.\

- Preferably, you should use a single `<h1>` per page—this is the top level heading, and all others sit below this in the hierarchy.
- Make sure you use the headings in the correct order in the hierarchy. Don't use `<h3>` elements to represent subheadings, followed by `<h2>` elements to represent sub-subheadings.
- Of the six heading levels available, you should aim to use no more than three per page, unless you feel it is necessary.

> - we need to make sure we are using the correct elements, giving our content the correct meaning, function, or appearance.
> - Semantics has nothing to do with the **LOOK** of the elements, sure the browser by default apply some default styling to elements based on there type, but for example you can style a `p` element to appear like `h1` element using CSS, but that will not change its semantic, it will stay a _paragraph_.

> [!IMPORTANT]
>
> - Always respect the **semantics**.
> - Use a single `h1` element per page.
> - Use at least a single paragraph.
> - Use _no more_ than **three** type of headings unless necessary.
> - Never choose semantic elements for their default style, if you only want to change the _look_ for something use _CSS_.

### ✅💻 02 - Vehicles

This is a fully text-based project, that introduce in a brief manner all the type of vehicles which is _air, road, water vehicles_, and under each type there is some _but not all_ types & vehicles.

- [code](/projects/html-stage/02-vehicles/)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/02-vehicles/index.html)

## Emphasis & Importance [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Emphasis_and_importance)

In HTML we use the `<em>` element to mark up **emphasis**.\
And we use `<strong>` element to mark up **importance**.

> **presentational elements** should no longer be used because, as we've seen before, semantics is so important to accessibility, SEO, etc.\
> For styling you should only use CSS.

> [!WARNING]
> There are [some others](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Emphasis_and_importance#italic_bold_underline%E2%80%A6) that are a bit confusing: `<b>, <i>, and <u>`,\
>  just forget about them now!

> [!IMPORTANT]
> Include `em` and `strong` at least once for each in your page.

## Lists [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Lists)

On the web, we have three types of lists: **unordered**, **ordered**, and **description** lists.

### Unordered lists

Unordered lists are used to mark up lists of items for which the order of the items doesn't matter.\
They are built using the `<ul>` element, which wrap all the list items, each list item should be wrapped in a `<li>` element.

> [!IMPORTANT]
> Include at least a single **unordered list**.

### Ordered lists

Ordered lists are lists in which the order of item _does_ matter.\
The markup structure is the same as for unordered lists, except that you have to wrap the list items in an `<ol>` element, rather than `<ul>`

> [!IMPORTANT]
> Include at least a single **ordered list**.

### Nesting lists

You can create an new list within another list by wrapping new `ol` or `ul` inside a `li` elem.

```html
<ol>
  <li>item 1</li>
  <li>item 2</li>
  <li>
    item 3
    <ul>
      <li>sub-item 1</li>
      <li>sub-item 2</li>
      <li>sub-item 3</li>
    </ul>
  </li>
</ol>
```

> [!IMPORTANT]
> Nest at least one list.
> It doesn't matter if it is nested in `ul` or `ol`.

### Description lists [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Lists#description_lists)

> The purpose of description lists is to mark up a set of items and their associated descriptions, such as terms and definitions, or questions and answers.

It is created by `<dl>`(description list) element,\
Each term is wrapped in a `<dt>` (description term) element,\
And each description definition is wrapped in a `<dd>` (description definition) elem.\

```html
<dl>
  <dt>description term</dt>
  <dd>description definition</dd>

  <dt>description term</dt>
  <dd>description definition</dd>

  <dt>description term</dt>
  <dd>description definition</dd>
</dl>
```

> [!IMPORTANT]
> Include at least a single **description list**.
