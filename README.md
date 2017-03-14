REPLACE BADGES !!!!!

[![Coverage Status](https://coveralls.io/repos/github/yoavniran/gulp-jest-jspm/badge.svg?branch=master)](https://coveralls.io/github/yoavniran/gulp-jest-jspm?branch=master)
[![npm Version](https://img.shields.io/npm/v/gulp-jest-jspm.svg)](https://www.npmjs.com/package/gulp-jest-jspm) 
[![CircleCI](https://circleci.com/gh/yoavniran/gulp-jest-jspm/tree/master.svg?style=svg)](https://circleci.com/gh/yoavniran/gulp-jest-jspm/tree/master)

# jest-jspm

A Helper to generate [Jest](https://facebook.github.io/jest/) configuration for a JSPM/SystemJS based application.
 Since System JS applies its own logic for how to resolve dependencies Jest cannot locate them while running.
 This library helps you test your app with Jest by generating the correct mappings configuration Jest understands.
 
## Usage

Install: 

 ```bash
 $ npm install --save-dev jest-jspm
 ```


In your code:

```javascript

import makeJestConfig from "jest-jspm";

const jestConfig = makeJestConfig({
	//...options
});

```

The options accepted by the make method are:


 > **jestConfig** - config object or string path to config json file (default: {})
 
 > **jestOptions** - config object passed to the Jest-CLI (for example {debug: true}) (default: undefined)
 
 > **systemJs** - location of system js (default: "./jspm_packages/system")
 
 > **sjsConfigFile** - location of System JS config file (default: "./config")
 
 > **loadSjsConfFile** - whether to load the System JS config file (default: true)
 
 > **jspmPackages** - location of jspm packages (default: "./jspm_packages")
 
 > **nodeModules** - location of node modules dir (default: "./node_modules")
 
 > **displayWarnings** - whether the plugin will output warnings to console (default: false)

 
This library is used by the following packages:

[gulp-jest-jspm](https://www.npmjs.com/package/gulp-jest-jspm)

[grunt-jest-jspm](https://www.npmjs.com/package/grunt-jest-jspm)