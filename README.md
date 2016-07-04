# fis-postprocessor-qunit-phantomjs [![Build Status](https://github.com/Milo-z/fis-postprocessor-qunit-phantomjs)](https://travis-ci.org/Milo-z/fis-postprocessor-qunit-phantomjs)

[![NPM](https://nodei.co/npm/fis-postprocessor-qunit-phantomjs?downloads=true)](https://nodei.co/npm/fis-postprocessor-qunit-phantomjs/)

> Run QUnit unit tests in a headless PhantomJS instance without using Grunt.

Run QUnit unit tests in a PhantomJS-powered headless test runner, providing basic console output for QUnit tests. Uses the [phantomjs](https://github.com/Obvious/phantomjs) node module and the [PhantomJS Runner QUnit Plugin](https://github.com/jonkemp/qunit-phantomjs-runner).

If you're using [gulp](https://github.com/gulpjs/gulp), you should take a look at the [gulp-qunit](https://github.com/jonkemp/gulp-qunit) plugin.


## Install

Install with [npm](https://github.com/Milo-z/fis-postprocessor-qunit-phantomjs)

globally:
```bash
$ npm install -g fis-postprocessor-qunit-phantomjs
```

or locally:
```bash
$ npm install --save-dev fis-postprocessor-qunit-phantomjs
```

## Usage

	fis.match("**/test/*.html", {
		postpackager: fis.plugin("qunit", options)
	})

## API

### qunit(path-to-test-runner[, options]);

Opens a test runner file in PhantomJS and logs test results to the console.

#### options.verbose

Type: `Boolean`  
Default: `none`  

Add list as test cases pass or fail to output.

#### options.phantomjs-options

Type: `Array`  
Default: `None`

These options are passed on to PhantomJS. See the [PhantomJS documentation](http://phantomjs.org/api/command-line.html) for more information.

#### options.page

Type: `Object`  
Default: `None`

These options are passed on to PhantomJS. See the [PhantomJS documentation](http://phantomjs.org/page-automation.html) for more information.

#### options.timeout

Type: `Number`  
Default: `5`

Pass a number or string value to override the default timeout of 5 seconds.


#### options.customRunner

Type: `String`
Default: `None`

A path to a custom PhantomJS runner script. A custom runner can be used to have more control over PhantomJS (configuration, hooks, etc.). Default runner implementations are provided by the [PhantomJS Runner QUnit Plugin](https://github.com/jonkemp/qunit-phantomjs-runner).

## License

MIT © [Milo-z])
