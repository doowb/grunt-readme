# grunt-readme [![NPM version](https://badge.fury.io/js/grunt-readme.png)](http://badge.fury.io/js/grunt-readme) 

> Grunt plugin for generating a README from templates, including an optional table of contents. No Gruntfile config is necessary, just choose a starter template and you'll be ready to go.

[Also see examples →](./EXAMPLES.md) and [documentation →](./DOCS.md)

Please [report any bugs or feature requests](https://github.com/helpers/grunt-readme/issues/new), thanks!

## Quickstart
_If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide._

From the same directory as your project's [Gruntfile][Getting Started] and [package.json][], install this plugin with the following command:

```bash
npm install grunt-readme --save-dev
```

Once that's done, add this line to your project's Gruntfile:

```js
grunt.loadNpmTasks('grunt-readme');
```

If the plugin has been installed correctly, run `grunt readme` at the command line. If the plugin has been installed properly, you should see a success message.

_**That's it!** If you are happy with the defaults, **no additional Gruntfile configuration is required**._


## Example README template
When you first add grunt-readme to a project, the task will automatically add a readme if it doesn't find one. But it's recommended that you customize you're own README template. Feel free to use [any of the templates](./templates) included in this repo, or copy/past the blow example into `./docs/README.tmpl.md`:

```js
# {%= name %}

> {%= description %}

{%= toc %}

## Overview
{%= _.doc("overview.md") %}

## Options
{%= _.doc("options.md") %}

## Examples
{%= _.doc("examples.md") %}

## License and Copyright
{%= copyright %}
{%= license %}
```

Then add `overview.md`, `options.md` and `examples.md` to the `./docs` directory. Of course, all of this is completely optional.

Visit the [full documentation →](./DOCS.md) | [See examples →](./DOCS.md#examples)


## Contributing
Please see the [Contributing to grunt-readme](https://github.com/assemble/grunt-readme/blob/master/CONTRIBUTING.md) guide for information on contributing to this project.

## Release History

 * 2013-11-15   v0.3.5   Repos task is now a separate grunt plugin. Adds basic badge mixins and lots of new test fixtures to test templates and mixins.
 * 2013-11-15   v0.3.0   Updates function that reads in metadata from options to accept mixed formats.
 * 2013-11-08   v0.2.4   Adds table of contents generation. Just use `{%= toc %}` where you want it to go.
 * 2013-11-03   v0.2.2   Fixes the function for the `metadata` option. Externalizes advanced docs since no config is really needed for this task.
 * 2013-10-11   v0.1.9   Adds ability to specify multiple metadata files in yaml or json format.
 * 2013-09-21   v0.1.3   Completely refactored. Adds a lot of documentation.
 * 2013-09-19   v0.1.0   First commmit.

## Test Mixins

* `{%= name %}`: grunt-readme
* `{%= shortname %}`: readme

## Author

+ [github.com/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter.com/jonschlinkert](http://twitter.com/jonschlinkert)

## License
Copyright (c) 2013 Jon Schlinkert, contributors.
Released under the MIT license

***

_This file was generated by [grunt-readme](https://github.com/assemble/grunt-readme) on Monday, December 16, 2013._


[grunt]: http://gruntjs.com/
[Getting Started]: https://github.com/gruntjs/grunt/blob/devel/docs/getting_started.md
[package.json]: https://npmjs.org/doc/json.html
