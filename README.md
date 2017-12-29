SublimeLinter-gjslint
=========================

[![Build Status](https://travis-ci.org/SublimeLinter/SublimeLinter-gjslint.svg?branch=master)](https://travis-ci.org/SublimeLinter/SublimeLinter-gjslint)

This linter plugin for [SublimeLinter](https://github.com/SublimeLinter/SublimeLinter) provides an interface to [gjslint](https://developers.google.com/closure/utilities/docs/linter_howto). It will be used with files that have the “JavaScript” syntax, or within `<script>` tags in HTML files.


## Installation
SublimeLinter must be installed in order to use this plugin. 

Please use [Package Control](https://packagecontrol.io) to install the linter plugin.

Before installing this plugin, you must ensure that `gjslint` is installed on your system. To install `gjslint`, do the following:

1. Install [Python](http://python.org).

1. Install `gjslint` by following the [installation instructions](https://developers.google.com/closure/utilities/docs/linter_howto).

In order for `gjslint` to be executed by SublimeLinter, you must ensure that its path is available to SublimeLinter. The docs cover [troubleshooting PATH configuration](http://sublimelinter.readthedocs.io/en/latest/troubleshooting.html#finding-a-linter-executable).


## Settings
- SublimeLinter settings: http://sublimelinter.readthedocs.org/en/latest/settings.html
- Linter settings: http://sublimelinter.readthedocs.org/en/latest/linter_settings.html

Additional SublimeLinter-gjslint settings: 

|Setting|Description|
|:------|:----------|
|jslint_error|A comma-separated list of specific lint errors to check|
|disable|A comma-separated list of error codes to ignore|
|max_line_length|The maximum allowed line length. `null` allows any length.|

We recommend configuring options in a .gjslintrc file (the linter will search for a config file with that name in your project path or ancestors). This is an example of a .gjslintrc file:
```
  --exclude_directories=reports,node_modules
  --exclude_files=Gruntfile.js
  --max_line_length=120
  --disable=5,240
  --custom_jsdoc_tags=namespace,version
```
For Closure Linter error codes, please see the [source code](https://code.google.com/p/closure-linter/source/browse/trunk/closure_linter/errors.py).
