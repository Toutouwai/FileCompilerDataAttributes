# File Compiler Data Attributes

A proof of concept module for populating markup elements according to data attributes containing a field name. Created in response to [this forum topic](https://processwire.com/talk/topic/21843-rendering-field-value-using-markup-attributes/). This approach is really only useful for text fields as far as I can see.

## Installation

[Install](http://modules.processwire.com/install-uninstall/) the File Compiler Data Attributes module.

## Setup

* If you follow the practice of starting your template files with the ProcessWire namespace declaration then for *every template* you want to use this module with you must change the "Use Compiled File?" option in the template settings from the default option. You must choose either of the "Yes" options depending on what suits you best. I find the need to do this annoying and there is [an open issue](https://github.com/processwire/processwire-issues/issues/882) about it. 

* There is an option in the module config to strip the `data-field` attribute from the markup when the template file is compiled.

## Usage

In your template files, insert HTML elements (probably empty elements although this is not compulsory) with a `data-field` attribute set according the field name you want to populate the element from.

Example:

```html
<h1 data-field="title"></h1>
<div data-field="body"></div>
```
