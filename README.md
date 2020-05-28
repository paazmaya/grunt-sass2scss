# grunt-sass2scss

> Convert Sass files to SCSS files with sass2scss

[![Build Status](https://img.shields.io/travis/paazmaya/grunt-sass2scss.svg?style=flat-square)](https://travis-ci.org/paazmaya/grunt-sass2scss)
[![devDependency Status](https://img.shields.io/david/dev/paazmaya/grunt-sass2scss.svg?style=flat-square)](https://david-dm.org/paazmaya/grunt-sass2scss#info=devDependencies)
[![Built with Grunt](http://img.shields.io/badge/Grunt-1.0-blue.svg?style=flat-square)](http://gruntjs.com/)
[![Using sass2scss](https://img.shields.io/badge/sass2scss-1.0-blue.svg?style=flat-square)](https://github.com/mgreter/sass2scss)

## Getting Started

This plugin requires [Grunt](http://gruntjs.com/) `~1.0.3` and [Node.js](https://nodejs.org/en/)
version to be minimum of `8.11.1`, which is [the active Long Term Support (LTS) version](https://github.com/nodejs/Release#release-schedule),
and `sass2scss` binary to be available either via `PATH` or defined via configuration.

The `sass2scss` tool can only [be compiled from sources](https://github.com/mgreter/sass2scss)
at the moment, for example in Linux/Mac:

```sh
wget https://github.com/mgreter/sass2scss/archive/v1.1.2.tar.gz
tar zxf v1.1.2.tar.gz
cd sass2scss-1.1.2/
make
[sudo] mv sass2scss /usr/local/bin/
```

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out
the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains
how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as
install and use Grunt plugins. Once you're familiar with that process, you may
install this plugin with this command:

```shell
npm install grunt-sass2scss --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-sass2scss');
```

## The "sass2scss" task

### Overview

In your project's Gruntfile, add a section named `sass2scss` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  sass2css: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    }
  }
});
```

### Options

#### options.binPath

Type: `String`

Default value: `'sass2scss'`

Path to the `sass2scss` binary, which by default is assumed to be found from
the system PATH.

#### options.args

Type: `Array`

Default value: `[]`

Command line options for the `sass2scss` command line utility.

```
-p, --pretty       pretty print output
-c, --convert      convert src comments
-s, --strip        strip all comments
-k, --keep         keep all comments
-h, --help         help text
-v, --version      version information
```

For example to set pretty printing and to keep comments, use `['-p', '-k']`, or
`['pretty', 'keep']`. The leading dashes are optional and added automatically when missing.

### Usage Examples

#### Default Options

```js
grunt.initConfig({
  sass2css: {
     defaultOptions: {
        files: {
          'tmp/default-1.scss': ['test/fixtures/styles-1.sass']
        }
      }
  }
});
```


## Contributing

["A Beginner's Guide to Open Source: The Best Advice for Making your First Contribution"](http://www.erikaheidi.com/blog/a-beginners-guide-to-open-source-the-best-advice-for-making-your-first-contribution/).

In lieu of a formal styleguide, take care to maintain the existing coding style.
Add unit tests for any new or changed functionality.
Lint and test your code using [Grunt](http://gruntjs.com/), via `grunt test` command.

[Also there is a blog post about "45 Github Issues Dos and Don’ts"](https://davidwalsh.name/45-github-issues-dos-donts).

Linting is done with [ESLint](http://eslint.org) and can be executed with `npm run lint`.
There should be no errors appearing after any JavaScript file changes.

## Release History

* `v0.4.0` (2018-12-16)
  - Minimum Node.js version lifted from `4.2.0` to `8.1.11`
  - Use Grunt.js minimum of `v1.0.3` and latest `sass2scss` which is `v1.1.2`
* `v0.3.1` (2016-08-13)
  - Dependencies are sure :tophat: up to date
  - Use ESLint directly without the Grunt.js plugin
* `v0.3.0` (2016-05-07)
  - It is Grunt.js `1.0.0` as the minimum supported
  - Start using shared ESLint configuration #3
* `v0.2.0` (2016-02-23)
  - Update dependencies
  - Minimum Node.js version requirement is `4.2.0` (LTS)
* `v0.1.1` (2015-01-26)
  - A bit more docs
* `v0.1.0` (2015-01-15)
  - Doing what is promised, when `sass2scss` is available

## License

Copyright (c) [Juga Paazmaya](https://paazmaya.fi) <paazmaya@yahoo.com>

Licensed under the [MIT license](LICENSE).
