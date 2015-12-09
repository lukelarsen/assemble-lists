[Assemble]:                http://assemblecss.com
[Assemble Core]:           https://github.com/lukelarsen/assemble-core

# Assemble Lists
Assemble Lists is a component of the [Assemble] CSS Framework. It will give you a solid base for using svg icons in your project. It has some default styles that can easily be overridden so you can add your own look.

## Requirements
Assemble Lists requires [Assemble Core].

## Installation
npm install assemble-lists --save-dev

## Usage
### Gulp
```js
var gulp = require('gulp');
var postcss = require('gulp-postcss');
var assembleCore = require('assemble-core');
var assembleLists = require('assemble-lists');

gulp.task('css', function () {
    var processors = [
        assembleCore,
        assembleLists
    ];
    return gulp.src('./src/*.css')
        .pipe(postcss(processors))
        .pipe(gulp.dest('./dest'));
});
```

## Options
Options are set with variables. These variables are already set with their default values so they will just work out of the box. If you wish to change them just define the variable you want to change before you load the _assemble-lists.css file. You may wish you see [Assemble Core] for more examples and directions for setting up a Assemble project.

### Design Variables

##### $list-colored-color
- Set the color for the bullet in colored lists.
- Default: #F00;
- Type: Color
```css
$list-colored-color: #000;
```

##### $list-colored-top
- Set the top space for the colored bullet in colored lists.
- Default: 3px;
- Type: Number
```css
$list-colored-top: 5px;
```

##### $list-colored-size
- Set the size of the colored bullet in colored lists.
- Default: 0.75em;
- Type: Number
```css
$list-colored-size: 10px;
```

##### $list-colored-padding-left
- Set the left padding of the colored bullet in colored lists.
- Default: 40px;
- Type: Number
```css
$list-colored-padding-left: 15px;
```

##### $list-col-colored-weight
- Set the weight of the ordered list numbers.
- Default: bold;
- Type: String
```css
$list-col-colored-weight: normal;
```

### Modifier Variables

##### $list-no-bullets
- Turn on/off a class that will remove bullets. If true a class of .list-no-bullets will be generated.
- Default: false;
- Type: Boolean
```css
$list-no-bullets: true;
```

##### $list-colored
- Turn on/off colored lists. This will allow you to color the bullets of a list. If true a class of .list-colored will be generated.
- Default: false;
- Type: Number
```css
$list-colored: true;
```
