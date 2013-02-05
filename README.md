# grunt-fontcustom [![Build Status](https://secure.travis-ci.org/MoOx/grunt-fontcustom.png?branch=master)](http://travis-ci.org/gruntjs/grunt-fontcustom)

> Compile SVG and EPS to Fonts (and CSS)


## Getting Started
If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide, as it explains how to create a [gruntfile][Getting Started] as well as install and use grunt plugins. Once you're familiar with that process, install this plugin with this command:

```shell
npm install grunt-fontcustom --save-dev
```

[grunt]: http://gruntjs.com/
[Getting Started]: https://github.com/gruntjs/grunt/blob/devel/docs/getting_started.md


## Fontcustom task
_Run this task with the `grunt fontcustom` command._

This task requires you to have [Ruby](http://www.ruby-lang.org/en/downloads/), [Fontcustom](http://fontcustom.github.com/fontcustom/) and its dependencies installed. If you're on OS X or Linux you probably already have Ruby installed, try `ruby -v` in your terminal. When you've confirmed you have Ruby installed, checkout [Fontcustom installation instructions](http://fontcustom.github.com/fontcustom/#installation) corresponding to your OS to install Fontcustom.

_This plugin is only compatible with Grunt `>= 0.4.x`._

### Options

#### src ```string```

Specify a source directory where are located .svg or .eps

#### dest ```string```

Specify an output directory. Default: {src}/../fontcustom.

#### name ```string```

Specify a font name. This will be used in the generated fonts and CSS. Default: fontcustom.

#### nohash ```boolean```

Disable filename hashes. Default: false.

[config]: http://fontcustom.github.com/fontcustom/#usage

### Usage Examples

#### Example config

```javascript
grunt.initConfig({
  fontcustom: {               // Task
    icons: {                   // Target
      options: {              // Target options
        src: 'icons/'
        dest: 'fonts/'
        name: 'icons',
      }
    }
  }
});

grunt.loadNpmTasks('grunt-fontcustom');

grunt.registerTask('default', ['jshint', 'fontcustom']);
```


## Release History

_(Nothing yet)_


---

Task submitted by [Maxime Thirouin](http://github.com/MoOx)

*This file was generated on Tue Feb 05 2013 09:32:26.*
