---
layout: layout
title: File extensions
---

File extensions
===============

Plates does not enforce a specific template file extension. By default it assumes `.php`. This file extension is automatically appended to your template names when rendered. You are welcome to change the default extension using one of the following methods.

## Constructor method

~~~.language-php
<?php

// Create new engine and set the default file extension to “.tpl”
$engine = new \League\Plates\Engine('/path/to/templates', 'tpl');
~~~

## Setter method

~~~.language-php
<?php

// Sets the default file extension to “.tpl” after engine instantiation
$engine->setFileExtension('tpl');
~~~

## Manually assign file extension

If you’d prefer to manually set the template file extension (ie. `$template->render('home.tpl')`), simply set the default file extension to `null`:

~~~.language-php
<?php

$engine->setFileExtension(null);
~~~