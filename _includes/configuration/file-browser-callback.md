## file_browser_callback

This option enables you to add your own file or image browser to TinyMCE.

If this option is set with a value a browse button will appear in different dialogs such as "insert/edit link" or "insert/edit image". If this option hasn't got a value set (or equals to false or null) the dialogs in question won't show any browse button.

This function is executed each time a user clicks on the "browse" buttons in various dialogs. The format of this callback function is: fileBrowser(field_name, url, type, win) where field_name is the id/name of the form element that the browser should insert its URL into. The url parameter contains the URL value that is currently inside the field. The type parameter contains what type of browser to present; this value can be file, image or flash depending on what dialog is calling the function. The win parameter contains a reference to the dialog/window that executes the function.

**Type:** `JavaScript Function`

##### Example

```js
tinymce.init({
  selector: 'textarea',  // change this value according to your HTML
  file_browser_callback: function(field_name, url, type, win) {
    win.document.getElementById(field_name).value = 'my browser value';
  }
});
```

You can fiddle with this example at the [{{site.tinymce_fiddle}}](http://{{site.tinymce_fiddle}}) site.
