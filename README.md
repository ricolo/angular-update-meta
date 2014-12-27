# Update meta tags in AngularJS

Dynamically update meta tags from within your markup in your AngularJS application.

[![Build Status](https://travis-ci.org/jvandemo/angular-update-meta.svg?branch=master)](https://travis-ci.org/jvandemo/angular-update-meta)

- lightweight (< 1KB)
- uses original meta syntax
- supports prerender.io for SEO purposes
- update your meta tags depending on the state your application is in
- no additional scripting required, works out-of-the-box!

## Usage

First install the module using bower:
 
```bash
$ bower install angular-update-meta
```

then add the `updateMeta` module to the dependencies of your AngularJS application module:

```javascript
angular.module('yourApp', ['updateMeta']);
```

Now you can use the following markup in your view(s):
 
```xml
<update-meta name="description" content="Meta description in head will now be updated with this string"></update-meta>
<update-meta http-equiv="content-type" content="text/some-content-type"></update-meta>
<update-meta charset="some-charset"></update-meta>
```

Only **existing** meta elements are updated.

If they don't exist yet, they are **NOT** added, so make sure they exist in your original `head` element.

## Contribute

To update the build in the `dist` directory:

```bash
$ gulp
```

To run the unit tests (for both concatenated and minified version):

```bash
$ gulp test
```

## Change log

### v1.2.0

- update bower ignore files

### v1.1.0

- add travis support
- update documentation

### v1.0.0

- refactor to support original markup
- add unit tests
- update documentation

### v0.1.0

- Initial version