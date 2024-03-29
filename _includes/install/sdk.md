### Step 1: Download the Self-hosted package

If you'd rather download and install the script manually, get the package from [TinyMCE Downloads]({{site.get-tiny}}).

Unzip the package and move the `'path/to/tinymce/'` directory into a web accessible location on your web server (for example, `localhost`).

### Step 2: Include the TinyMCE script

Include this line of code in the `<head>` of your HTML page:

```html
<script src="path/to/tinymce/js/tinymce.min.js"></script>
```

### Step 3: Initialize TinyMCE as part of a web form

With the script included, initialize TinyMCE on any element (or elements) in your web page.

Since TinyMCE lets you identify replaceable elements via a CSS selector, all you need do is pass an object that contains a `selector` to `tinymce.init()`.

In this example, let's replace `<textarea id='mytextarea'>` with a TinyMCE editor instance by passing the selector `'#mytextarea'` to `tinymce.init()`.

```html
<!DOCTYPE html>
<html>
<head>
  <script src="/path/to/tinymce/tinymce.min.js"></script>
  <script type="text/javascript">
  tinymce.init({
    selector: '#mytextarea'
  });
  </script>
</head>

<body>
<h1>TinyMCE Quick Start Guide</h1>
  <form method="post">
    <textarea id="mytextarea">Hello, World!</textarea>
  </form>
</body>
</html>
```

### Step 4: Saving content with a form POST

When the `<form>` is submitted the TinyMCE editor mimics the behavior of a normal HTML `<textarea>` during the `post`. In your form handler you can process the content submitted as if it had come from a regular `<textarea>`.

> If you decided to use the Self-hosted package, move on to the next step [working with plugins](../work-with-plugins/), where you'll start customizing TinyMCE. If you'd like to learn about other install options please keep reading.
