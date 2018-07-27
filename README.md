# Pug-Sass Starter

A simple starter for building HTML templates with Pug and Sass.

## Requirements

Make sure [Node JS](https://nodejs.org), [NPM](https://www.npmjs.com) and [Gulp](http://gulpjs.com/) already installed on your computer.

## Install

* Navigate to the directory where the _pug-sass-starter_ folder is located using **Terminal**.
* Execute `npm install`.

## Run

* Execute `npm start` or `gulp`.
* Open `http://localhost:8080/` on your web browser.

## 3rd Party Libraries

If you wannna add 3rd party library to your project, install the library using npm, and then include it on `gulpfile.js ` file, please see code below for example.

```js
var vendorStyles = [
  // 3rd party styles here, if possible use minified version files please.
  'node_modules/bootstrap/dist/css/bootstrap.min.css'
 ];
 
 var vendorScripts = [
  // 3rd party scripts here, if possible use minified version files please.
  'node_modules/bootstrap/dist/js/bootstrap.min.js'
 ];
```

There are already gulp tasks that will minifying and concating all of your 3rd party libraries, you just need to execute `gulp styles-combine`, `gulp scripts-combine` or `gulp combine`, wait for a moment and it will automatically creates `vendors.min.css` and `vendors.min.js` inside `assets` folder. Do not forget to include vendors files on `base.pug` file. Finally, run your project using `npm start` or `gulp`.

## Folders Structure

```
+ assets
  + css : This folder contains prebuild files, styles.css and styles.min.css.
  + fonts : Place your fonts here, also do not forget to import it on _variables.scss.
  + icons : Place your icons here.
  + images : Place your images here.
  + js : This folder contains prebuild files, scripts.js and scripts.min.js.
+ src
  + js
    - scripts.js : Store your js code here.
  + pug
    + base
      - base.pug : Base pug file.
    + layouts
      - default-layout.pug : Default layout pug file.
      - footer.pug : Footer pug file.
      - header.pug : Header pug file.
    + pages
      - index.pug : Example page pug file, it contains h1 only.
  + sass
    + base
      - _global.scss : Global styles for html, body, section, headings, anchor etc.
      - _mixins.scss : Store your mixins here;
      - _placeholders.scss : Store your placeholders here;
      - _variables.scss : Store your variables here;
    + components
      - _components.scss : It contains components styles such as buttons, modals etc.
    + layouts
      - _footer.scss : It contains footer styles.
      - _header.scss : It contains header styles.
    + pages
      - _index.scss : Example scss for specific page.
    - styles.scss : Import all scss files.
- index.html : Prebuild HTML file, other HTML files will be placed here too.
```

## Gulp Plugins

* [gulp-connect](https://www.npmjs.com/package/gulp-connect) : Run webserver (with livereload).
* [gulp-plumber](https://www.npmjs.com/package/gulp-plumber) : Prevent pipe breaking caused by errors from gulp plugins.
* [gulp-pug](https://www.npmjs.com/package/gulp-pug) : Gulp plugin for compiling Pug templates, compile Pug into HTML.
* [gulp-rename](https://www.npmjs.com/package/gulp-rename) : Gulp plugin to rename files easily, adding `.min` suffix.
* [gulp-sass](https://www.npmjs.com/package/gulp-sass) : Compile your SCSS into CSS.
* [gulp-uglify](https://www.npmjs.com/package/gulp-uglify) : Minify your JS.
* [gulp-clean-css](https://www.npmjs.com/package/gulp-clean-css) : Minify your CSS.
* [gulp-concat](https://www.npmjs.com/package/gulp-concat) : Concating your files.