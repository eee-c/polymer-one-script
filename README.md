# polymer-one-script for Polymer.dart

A simple Dart script to rewrite the output of Polymer.dart `pub build` output so that a single JavaScript file, with all templates, is produced.  The resulting JavaScript file should be deployable for use on any page on the modern web.

## Usage

Add `polymer_one_script` to the list of you application's `pubspec.yaml':

```yaml
name: application_name_here
dev_dependencies:
  polymer_one_script: any
transformers:
- polymer:
    entry_points:
      - web/index.html
```

After a `pub update`, copy the script into your application's bin directory:

```
$ mkdir bin
$ cop packages/polymer_one_script/polymer-one-script bin
$ chmod a+x bin/polymer-one-script
```

Run this after a Pub build: `pub build; ./bin/polymer-one-script`.

## TODO

This is a very early release. Much is sure to go wrong. The following could almost certainly use some help:

 * This almost certainly won't work on Windows
 * The escaping of the templates is weak. Single quotes will probably break things :-\

## License

MIT.
