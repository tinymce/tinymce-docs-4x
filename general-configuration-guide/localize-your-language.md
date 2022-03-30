---
layout: default
title: 10. Localize TinyMCE
description: Localize TinyMCE with global language capabilities.
keywords: internationalization localization languages
---

As developers, we all hope our projects reach the wider audience, and for many of us, they do. This is why it is vital that TinyMCE is easy to localize its language.

In this section, we show you how to change TinyMCE's user interface to suit your users' preferred language. The settings discussed in this section change the language that toolbar and menubar items, along with tooltips, are rendered in.


> Pro tip: Language settings can be controlled in these configuration options: [directionality]({{ site.baseurl }}/configure/localization/#directionality), [language]({{ site.baseurl }}/configure/localization/#language) and  [language_url]({{ site.baseurl }}/configure/localization/#language_url). There is also a [Directionality Plugin]({{ site.baseurl }}/plugins/directionality/) that adds a toolbar button to control `ltr-rtl` behavior.

### Step 1

Download the [Tinymce 4 language pack](/language/tinymce4x_languages.zip) (i18n), which contains the fullset of languages supported by TinyMCE 4.

> Note: The TinyMCE 4 community translation packs are no longer maintained

### Step 2

Unpack the language `js` file(s) into your `path/to/tinymce/langs/` folder.

> Important: If you don't put the language pack in `langs/`, the language settings will not work unless you use the [language_url]({{ site.baseurl }}/configure/localization/#language_url) configuration option.

### Step 3

Set the language option in your TinyMCE configuration to the language code in the list on [this page]({{ site.baseurl }}/configure/localization/#language).

### Step 4

Confirm that the language has been set successfully by loading TinyMCE.


## A working example

We have prepared a code snippet below that would set TinyMCE's language to Chinese and text directionality right-to-left.

If you want to try it for yourself, [download the TinyMCE 4 language pack](/language/tinymce4x_languages.zip), unzip the file and place the ```zh_CN.js``` file in your ```tinymce/lang``` folder. If you don't have TinyMCE setup, you can grab a copy from our [downloads page]({{site.get-tiny}}). Follow the [Self-hosted install instructions]({{ site.baseurl }}/general-configuration-guide/advanced-install/#sdkinstall) if you're not familiar with setting up TinyMCE locally.

```html
<!DOCTYPE html>
<html>
<head>
  <script src="js/tinymce.min.js"></script>
  <script type="text/javascript">
  tinymce.init({
    selector: 'textarea',
    language: 'zh_CN',
    directionality: 'rtl'
  });
  </script>
</head>

<body>
  <form method="post">
    <textarea>你好，世界!</textarea>
  </form>
</body>
</html>
```

{% assign_page next_page = "/general-configuration-guide/system-requirements/index.html" %}
{% include next-step.html next=next_page %}
