---
layout: default
title: How to setup the homepage demos
title_nav: Setup homepage demos
description_short: How to setup the example demos on the homepage.
description: How to setup the example demos on the homepage
keywords: demo cms lms email template tinymce
---

## <a name="cms" id="cms"></a>Setup the CMS/Blog example

The CMS demo highlights some of the most common TinyMCE deployment scenarios, including for Content Management Systems, Blogs, Learning Management Systems, and more. These environments typically involve the online creation of content for online consumption. They also share several commonalities including:

* The desire for the platform to render similar fidelity to source content in the browser.
* The need to solve common workflows (e.g. copy/pasting content from Word or the internet).
* Helping non-technical users create clean, modern, and valid HTML content without knowing “how to code”.

### Technical Overview
Platforms like Blogs and Content Management Systems are focused on creating content to be consumed via the web (browsers, mobile devices, etc).  When generating content for consumption on the web one can use all of the features and flexibility available in TinyMCE to allow as rich a content authoring experience as desired.

When deploying TinyMCE for this use case you should spend some time analyzing what features of TinyMCE are truly useful for your content creation scenarios - only show the capabilities needed to assist your content authors in getting their job done.

### Community plugins used in this demo:

* [link](https://www.tinymce.com/docs/plugins/link/)
* [lists](https://www.tinymce.com/docs/plugins/lists/)
* [table](https://www.tinymce.com/docs/plugins/table/)

### Pro plugins used in this demo:

#### [Advanced Code Editor](https://www.tinymce.com/docs/plugins/advcode/)
Do you have advanced users that want to see and manipulate the HTML itself?  Our Advanced Code Editor provides a color coded easy-to-use interface to edit the HTML while in the content authoring process.

#### [Enhanced Media Embeds](https://www.tinymce.com/docs/plugins/mediaembed/)
Do your authors want to insert references to platforms like Twitter, YouTube, Facebook, or SlideShare?  Our Enhanced Media Embed plugin makes creating such content as simple as copying and pasting a link!

#### [Link Checker](https://www.tinymce.com/docs/plugins/linkchecker/)
Broken links are never a good thing!  Nobody wants to publish content with broken links.  Our Link Checker plugin allows you to provide real time link checking to your content authors as they create content so they can correct broken links before they are ever published!

#### [MoxieManager](https://www.tinymce.com/docs/plugins/moxiemanager/)
Do you want people to insert and manage rich media like images/videos?  MoxieManager makes that process simple and efficient for your content authors!

#### [PowerPaste](https://www.tinymce.com/docs/plugins/powerpaste/)
Do you want authors to be able to use Word and/or Excel documents as the basis for content? PowerPaste makes the copy/paste process simpler for the author while providing you with semantically correct and clean HTML.

#### [Spell Checker Pro](https://www.tinymce.com/docs/plugins/tinymcespellchecker/)
Nobody likes to see misspelled words in their content. Our Spell Checker Pro plugin allows you to provide real time spell checking to your content authors as they create content.

### Quick Configuration

```javascript
  tinymce.init({
      width: 930,
      height: 273,
      powerpaste_word_import: "prompt",
      powerpaste_html_import: "clean",
      spellchecker_language: "en",
      resize: false,
      statusbar: false,
      plugins: [
          'advcode',
          'link',
          'linkchecker',
          'lists',
          'mediaembed',
          'powerpaste',
          'table',
          'tinymcespellchecker'
       ],
      autoresize_bottom_margin: 1,
      menubar: false,
      toolbar: "undo redo | formatselect | bold italic strikethrough | alignleft aligncenter alignright | bullist numlist | indent outdent | link table"
  });
```

> Quick add this config to the [Tiny Configurator](#).

### Advanced config options used in this demo

```javascript
powerpaste_word_import: "clean"
```
When pasting content from a Word document, Word typically includes a variety of inline styles.  These styles (if left in place) make it hard for an online system like a Blog or CMS to get a consistent look and feel across all content items.  The `clean` setting allows you keep the semantic structure of the document while removing all the inline styles.

```javascript
powerpaste_html_import: "clean"
```

When pasting content from another web page (HTML) it is common that the HTML you are pasting would include a variety of inline styles and classes that are specific to the source HTML page .  These styles (if left in place) make it hard for an online system like a Blog or CMS to get a consistent look and feel across all content items.  The `clean` setting allows you keep the semantic structure of the HTML content while removing all the inline styles.




## <a name="doccreator" id="doccreator"></a>Setup the Document Creator example
The Document Creator demo highlights our new PDF Export plugin, rendering a screen representation of this common portable document output. It solves for use cases where content is created online but where the end-user consumes the content in a portable document format such as Adobe PDF. This is useful where the content is shared outside the content creation workflow or printed to paper.

### Technical Overview
A common use case for online content creation is that the information created online will be converted to a traditional document format such as a Word document or a PDF.  When generating content for this scenario you can style the editor to visually resemble a fixed with format (e.g. A4 or US Letter paper) and you can limit the capabilities exposed via the toolbar to ensure that the content created can be easily converted to these other formats.

### Community plugins used in this demo:

* [advlist](https://www.tinymce.com/docs/plugins/advlist/)
* [directionality](https://www.tinymce.com/docs/plugins/directionality/)
* [image](https://www.tinymce.com/docs/plugins/image/)
* [link](https://www.tinymce.com/docs/plugins/link/)
* [lists](https://www.tinymce.com/docs/plugins/lists/)
* [pagebreak](https://www.tinymce.com/docs/plugins/pagebreak/)
* [table](https://www.tinymce.com/docs/plugins/table/)
* [textcolor](https://www.tinymce.com/docs/plugins/textcolor/)

### Pro plugins used in this demo:

### [Link Checker](https://www.tinymce.com/docs/plugins/linkchecker/)
Broken links are never a good thing!  Nobody wants to publish a document with broken links.  Our Link Checker plugin allows you to provide real time link checking to your document authors as they create their documents so they can correct broken links before they are ever published!

### [PowerPaste](https://www.tinymce.com/docs/plugins/powerpaste/)
Do you want authors to be able to use Word and/or Excel content as the basis for their document? PowerPaste makes the copy/paste process simpler for the author while providing you with semantically correct and clean HTML.

### [Spell Checker Pro](https://www.tinymce.com/docs/plugins/tinymcespellchecker/)
Nobody likes to see misspelled words in their documents. Our Spell Checker Pro plugin allows you to provide real time spell checking to your content authors as they create their documents.

### Quick Configuration

```javascript
  tinymce.init({
      width: 930,
      height: 273,
      powerpaste_word_import: "prompt",
      powerpaste_html_import: "clean",
      spellchecker_language: "en",
      resize: false,
      content_css: 'http://10.1.20.104/web/document.css',
      status_bar: false,
      toolbar: 'undo redo | formatselect | fontselect | fontsizeselect | bold italic underline | link unlink | alignleft aligncenter alignright | bullist numlist | indent outdent | removeformat',
      plugins: [
          'advlist',
          'directionality',
          'image',
          'link',
          'linkchecker',
          'lists',
          'pagebreak',
          'table',
          'textcolor',
          'powerpaste',
          'tinymcespellchecker'
      ]
  });
```

> Quick add this config to the [Tiny Configurator](#).

### Advanced config options used in this demo

```javascript
powerpaste_word_import: "prompt"
```

When pasting content from a Word document, Word typically includes a variety of inline styles.  Depending upon your use case you may wish to...
* Include these styles to allow more bespoke styling and formatting within the document
* Remove these styles to enforce a more standard style and formatting

The `prompt` setting allows the author to choose whether to keep or remove the styles when the content is pasted into TinyMCE based on their specific use case.

```javascript
powerpaste_html_import: "clean"
```
When pasting content from another web page (HTML) it is common that the HTML you are pasting would include a variety of inline styles and classes that are specific to the source HTML page .  These styles (if left in place) make it hard to get a consistent look and feel across all documents.  The `clean` setting allows you keep the semantic structure of the HTML content while removing all the inline styles.




## <a name="email" id="email"></a>Setup the Email example
The email demo highlights environments where content is consumed in an email client, where the client significantly restricts the HTML and CSS that can be rendered for the purposes of consistency across platforms. This is a common use case where there is a requirement to restrict HTML and CSS to specific elements that that work across common email clients.  


### Technical Overview
When creating HTML and CSS to be consumed by email clients it is important to realize that a great many options available in HTML and CSS are not allowed by some of the more commonly used email clients.  When allowing someone to create an email it is imperative that you configure TinyMCE to only allow the content author to create HTML and CSS that will work in email clients.  

You can limit the options provided on the toolbars and menubar to help limit the type of content created.  You can also use some TinyMCE configuration settings to further control the tags, classes, and styles added to the content. These would include:

* `valid_elements`: [see config](https://www.tinymce.com/docs/configure/content-filtering/#valid_elements)
* `valid_children`: [see config](https://www.tinymce.com/docs/configure/content-filtering/#valid_children)
* `valid_classes`: [see config](https://www.tinymce.com/docs/configure/content-filtering/#valid_classes)
* `valid_styles`: [see config](https://www.tinymce.com/docs/configure/content-filtering/#valid_styles)
* `extended_valid_elements`: [see config](https://www.tinymce.com/docs/configure/content-filtering/#extended_valid_elements)


### Community plugins used in this demo:

* [autolink](https://www.tinymce.com/docs/plugins/autolink/)
* [contextmenu](https://www.tinymce.com/docs/plugins/autolink/)
* [link](https://www.tinymce.com/docs/plugins/link/)
* [lists](https://www.tinymce.com/docs/plugins/lists/)
* [textcolor](https://www.tinymce.com/docs/plugins/textcolor/)

### Pro plugins used in this demo:

### [Link Checker](https://www.tinymce.com/docs/plugins/linkchecker/)
Broken links are never a good thing!  Nobody wants to publish an email with broken links.  Our Link Checker plugin allows you to provide real time link checking to your document authors as they create their emails so they can correct broken links before they are ever sent!

### [PowerPaste](https://www.tinymce.com/docs/plugins/powerpaste/)
Do you want authors to be able to use Word and/or Excel documents as the basis for their emails? PowerPaste makes the copy/paste process simpler for the author while providing you with semantically correct and clean HTML making it easier to create emails that look great in all email clients.

### [Spell Checker Pro](https://www.tinymce.com/docs/plugins/tinymcespellchecker/)
Nobody likes to see misspelled words in their emails. Our Spell Checker Pro plugin allows you to provide real time spell checking to your content authors as they create their emails.

### Quick Configuration

#### Heading:
 ```javascript
  tinymce.init({
      selector: '.tinymce-heading',
      menubar: false,
      inline: true,
      plugins: [
        'autolink',
        'contextmenu',
        'link',
        'linkchecker',
        'lists',
        'powerpaste',    
        'textcolor',
        'tinymcespellchecker'
      ],
      toolbar: 'undo redo | bold italic underline | link unlink',
      valid_elements: 'strong,em,span[style],a[href]',
      valid_styles: {
        '*': 'font-size,font-family,color,text-decoration,text-align'
      },
      powerpaste_word_import: 'clean',
      powerpaste_html_import: 'clean'
  });
```

#### Body

```javascript
  tinymce.init({
      selector: '.tinymce-body',
      menubar: false,
      inline: true,
      plugins: [
        'link',
        'textcolor',
        'lists',
        'powerpaste',
        'linkchecker',
        'contextmenu',
        'autolink',
      ],
      toolbar: [
        'undo redo | bold italic underline | fontselect fontsizeselect',
        'forecolor backcolor | alignleft aligncenter alignright alignfull | link unlink | numlist bullist outdent indent'
      ],
      valid_elements: 'p[style],strong,em,span[style],a[href],ul,ol,li',
      valid_styles: {
        '*': 'font-size,font-family,color,text-decoration,text-align'
      },
      powerpaste_word_import: 'clean',
      powerpaste_html_import: 'clean'
  });
```

> Quick add this config to the [Tiny Configurator](#).

### Advanced config options used in this demo

```javascript
valid_elements: 'p[style],strong,em,span[style],a[href],ul,ol,li'
```

Many email clients support only a subset of modern HTML and CSS.  This setting allows you to configure which HTML tags and attributes will be considered valid in the HTML.  Any attempt to insert any other HTML tags (via pasting, code view, etc) will be removed automatically by TinyMCE.

```javascript
valid_styles: {'*': 'font-size,font-family,color,text-decoration,text-align'}
```

Many email clients support only a subset of modern HTML and CSS.  This setting allows you to configure which CSS styles will be considered valid within the `style` element in each tag.  Any attempt to insert any other CSS (via pasting, code view, etc) will be removed automatically by TinyMCE.

```javascript
powerpaste_word_import: "clean"
```

When pasting content from a Word document, Word typically includes a variety of inline styles.  These styles (if left in place) make it hard to get a consistent look and feel across various emails created using TinyMCE.  The clean setting allows you keep the semantic structure of the document while removing all the inline styles leading to a more consistent look and feel across the emails you create.

```javascript
powerpaste_html_import: "clean"
```

When pasting content from another web page (HTML) it is common that the HTML you are pasting would include a variety of inline styles and classes that are specific to the source HTML page.  These styles (if left in place) make it hard to get a consistent look and feel across various emails created using TinyMCE.  The clean setting allows you keep the semantic structure of the document while removing all the inline styles leading to a more consistent look and feel across the emails you create.




## <a name="distractionfree" id="distractionfree"></a>Setup the Distraction-Free example
The distraction-free demo highlights ...  

### Technical Overview
Many modern content platforms are looking for a lightweight user interface that skips the traditional toolbars and menubars and instead provides you with context appropriate assistance in real time. The TinyMCE [inlite](https://www.tinymce.com/docs/themes/inlite/) theme makes it easy for you to provide this type of user interface to your content authors.  In this scenario instead of the traditional toolbar configuration
you have two toolbars that you can configure to the specific needs when inserting new a new paragraph/block and when you highlight existing content:

* [Insert Toolbar](https://www.tinymce.com/docs/configure/editor-appearance/#insert_toolbar):  This toolbar appears appears when create a new block within the content
* [Selection Toolbar](https://www.tinymce.com/docs/configure/editor-appearance/#selection_toolbar): This toolbar appears when you highlight/select existing content in the editor

### Community plugins used in this demo:

* [autolink](https://www.tinymce.com/docs/plugins/autolink/)
* [link](https://www.tinymce.com/docs/plugins/link/)
* [lists](https://www.tinymce.com/docs/plugins/lists/)
* [textcolor](https://www.tinymce.com/docs/plugins/textcolor/)

### Pro plugins used in this demo:

#### [Enhanced Media Embeds](https://www.tinymce.com/docs/plugins/mediaembed/)
Do your authors want to insert references to platforms like Twitter, YouTube, Facebook, or SlideShare?  Our Enhanced Media Embed plugin makes creating such content as simple as copying and pasting a link!

### [Link Checker](https://www.tinymce.com/docs/plugins/linkchecker/)
Broken links are never a good thing!  Nobody wants to publish articles with broken links.  Our Link Checker plugin allows you to provide real time link checking to your content authors as they create their articles so they can correct broken links before they are ever published!

### [PowerPaste](https://www.tinymce.com/docs/plugins/powerpaste/)
Do you want authors to be able to use Word and/or Excel documents as the basis for their articles? PowerPaste makes the copy/paste process simpler for the author while providing you with semantically correct and clean HTML making it easier to create content that looks consistent across all of your articles.

### [Spell Checker Pro](https://www.tinymce.com/docs/plugins/tinymcespellchecker/)
Nobody likes to see misspelled words in their articles. Our Spell Checker Pro plugin allows you to provide real time spell checking to your content authors as they create their articles.

### Quick Configuration

#### Heading:

 ```javascript
  tinymce.init({
      selector: '.tinymce-heading',
      menubar: false,
      inline: true,
      theme: 'inlite',
      insert_toolbar: 'undo redo',
      selection_toolbar: 'italic underline',
      plugins: [
        'tinymcespellchecker'
      ],
  });
```

#### Body

```javascript
tinymce.init({
  selector: '.tinymce-body',
  menubar: false,
  inline: true,
  theme: 'inlite',
  plugins: [
    'autolink',
    'link',
    'linkchecker',
    'lists',
    'mediaembed',
    'powerpaste',
    'textcolor',
    'tinymcespellchecker'
  ],
  toolbar: [
    'undo redo | bold italic underline | fontselect fontsizeselect',
    'forecolor backcolor | alignleft aligncenter alignright alignfull | link unlink | numlist bullist outdent indent'
  ],
  insert_toolbar: 'h2 h3 | bold italic | quickimage | media',
  selection_toolbar: 'bold italic | quicklink h1 h2 h3 | blockquote | code a11ycheck | media',
  powerpaste_word_import: 'clean',
  powerpaste_html_import: 'clean'
});
```

> Quick add this config to the [Tiny Configurator](#).

### Advanced config options used in this demo

```javascript
powerpaste_word_import: "clean"`
```

When pasting content from a Word document, Word typically includes a variety of inline styles.  These styles (if left in place) make it hard to get a consistent look and feel across various emails created using TinyMCE.  The clean setting allows you keep the semantic structure of the document while removing all the inline styles leading to a more consistent look and feel across the emails you create.

```javascript
powerpaste_html_import: "clean"
```

When pasting content from another web page (HTML) it is common that the HTML you are pasting would include a variety of inline styles and classes that are specific to the source HTML page.  These styles (if left in place) make it hard to get a consistent look and feel across various emails created using TinyMCE.  The clean setting allows you keep the semantic structure of the document while removing all the inline styles leading to a more consistent look and feel across the emails you create.
