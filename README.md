lintel-contrib-tables
=====================

> Tables for lintel.

[![npm](https://img.shields.io/npm/v/lintel-contrib-tables.svg)](https://github.com/lintelio/lintel-contrib-tables)
[![Bower](https://img.shields.io/bower/v/lintel-contrib-tables.svg)](https://github.com/lintelio/lintel-contrib-tables)


## Getting Started
This module requires Lintel.

If you haven't used [Lintel](http://lintel.io/) before, be sure to check out the [Getting Started](http://lintel.io/getting-started) guide, as it explains how to install and use this module. Once you're familiar with that process, you may install this module with this command:

```shell
bower install lintel-contrib-tables --save
```

Once the module has been installed, you will have to load it in your main SASS file:

```scss
@import "bower_components/lintel-contrib-tables/sass/tables.scss"
```

You can use [wiredep](https://github.com/taptapship/wiredep) or [grunt-wiredep](https://github.com/stephenplusplus/grunt-wiredep) to automatically inject files in your build process.


## Variables
Check the vars file in the `sass` folder to see the full list of variables you can customize.

#### $table-padding-y-base
Table cell padding-top and padding-bottom.

#### $table-padding-x-base
Table cell padding-left and padding-right.

#### $table-border
Default value: `$border-base`  

Border color.

#### $table-border-th
Default value: `$border-dakrest`  

Border under table head.

#### $table-divided-border
Default value: `$table-border`  

Vertical divider border color. Can also use `$table-divided-border-style` to change to `dotted` or `dashed`.

#### $table-striped-bg
Default value: `$bg-light`  

Striped table background.

#### $table-hover-bg
Default value: `$bg-base`  

`<td>` background on row hover.


#### $table-edge-padding-x
Default value: `$table-padding-x-base + $cushion-base`  

Changes the padding-left of the first column and the padding-right of the last column. This can be useful if you use a grid and want the table to expand to the edge (gutter). 

For example, you could change it to something like: `$table-padding-x-base + $grid-gutter` and place it outside of the column or have a class with negative margins to pull it out of the gutter.

If set to `0`, the `.table-edge` selectors will not be compiled in the CSS.


## Mixins
Check the mixins file in the `sass` folder to see how you can extend this module.

#### table-size($className, $padding-y, $padding-x)
Creates a new table-size class.

```scss
@include table-size("table-xl", 30px, 40px);
```

```css
.table-xl > thead > tr > th, 
.table-xl > thead > tr > td, 
.table-xl > tbody > tr > th, 
.table-xl > tbody > tr > td, 
.table-xl > tfoot > tr > th, 
.table-xl > tfoot > tr > td {
  padding: 12px 20px;
}
```


## Examples

#### Base
```html
<table class="table">
  <thead>
    <tr>
      <th>Heading 1</th>
      <th>Heading 2</th>
      <th>Heading 3</th>
      <th>Heading 4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell 1</td>
      <td>Cell 2</td>
      <td>Cell 3</td>
      <td>Cell 4</td>
    </tr>
    <tr>
      <td>Cell 1</td>
      <td>Cell 2</td>
      <td>Cell 3</td>
      <td>Cell 4</td>
    </tr>
    <tr>
      <td>Cell 1</td>
      <td>Cell 2</td>
      <td>Cell 3</td>
      <td>Cell 4</td>
    </tr>
  </tbody>
</table>
```

#### Modifiers
```html
<table class="table table-bordered table-divided table-edge table-hover table-striped">
  ...
</table>
```

#### States
```html
<table class="table">
  <thead>
    <tr>
      <th>Heading 1</th>
      <th>Heading 2</th>
      <th>Heading 3</th>
      <th>Heading 4</th>
    </tr>
  </thead>
  <tbody>
    <tr class="table-primary">
      <td>Primary BG 1</td>
      <td>Primary BG 2</td>
      <td>Primary BG 3</td>
      <td>Primary BG 4</td>
    </tr>
    <tr>
      <td>Cell 1</td>
      <td>Cell 2</td>
      <td>Cell 3</td>
      <td class="table-success">Success BG 4</td>
    </tr>
  </tbody>
</table>
```

#### Condensed
```html
<table class="table table-sm">
  ...
</table>
```


## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).


## License
Copyright (c) 2015 Marius Craciunoiu. Licensed under the MIT license.
