# Bootstrap for Pub

[![Build Status](https://travis-ci.org/richerlariviere/bootstrap_for_pub.svg?branch=master)](https://travis-ci.org/richerlariviere/bootstrap_for_pub)

Just a pub package of Bootstrap,
"The most popular front-end framework
for developing responsive, mobile first
projects on the web."

Currently contains Bootstrap 4.0.0-alpha.6

## Installation

See the [install instructions][install].

## Usage

You can include the bootstrap stylesheets and script once you have added this package as a 
dependency to your application:

```html
    <!-- include the stylesheets -->
    <link rel="stylesheet" href="packages/bootstrap/css/bootstrap.css">
    
    <!-- include the javascript -->
    <script src="packages/bootstrap/jquery/jquery.js"></script>
    <script src="packages/bootstrap/js/bootstrap.js"></script>
```

Note that the versions in the snippets above are the non-minified version.
The transformer available
in this package will automatically rewrite the URI to point to the minified
versions when pub is invoked in release mode.

To activate the transformer, update your `pubspec.yaml`

```yaml
transformers:
- bootstrap:
    url: //maxcdn.bootstrapcdn.com/bootstrap/{{version}}
    version: 4.0.0-alpha.6
```

The transformer takes up to two optional parameters:
- `url`: when specified the local base url (`packages/bootstrap/`) will be
   replaced by the given url. This is useful to automatically switch to
   using a CDN for your production environment.
- `version`: when specified, the sub-string "{{version}}" in the `url`
   parameter will be replaced with its value.

## Learn more

Visit the official [Bootstrap homepage][bs] for docs and more.

See LICENSE.

[install]: https://pub.dartlang.org/packages/bootstrap#installing
[bs]: https://v4-alpha.getbootstrap.com/
