# Getting Started

## Installation

**kolessal** is available via [**bower**].

```
$ bower install kolessal --save
```

<small>\* *The `--save` option persists kolessal to your `bower.json`*</small>

If you're using LESS, you can simply `include` either the LESS (if you compile stuff on your own) or the CSS file.

```less
@include "/path/to/kolessal/src/main.less"
# or
@include "/path/to/kolessal/dist/kolessal.css"
```

Otherwise, you can directly add it as a stylesheet to your HTML file.

```html
<link href="/path/to/kolessal/dist/kolessal.css" ref="stylesheet">
```

## Usage

You can probably figure out easily how this project works if you're familiar with RSCSS.

### `u-text`

Provides text utilities such as alignment, uppercase / lowercases, etc.

```html
<p class="u-text -center"></p>
<p class="u-text -left"></p>
<p class="u-text -right"></p>
<p class="u-text -up"></p>
<p class="u-text -low"></p>

<!--
  This styling cuts down text to a one-liner, and then
  ends overflowing text with an ellipsis
-->
<p class="u-text -truncate">
  This is a very long text that is cut down to one-line,
  and overflowing text is ended with an elipssi..
</p>

<!-- Altogether now -->
<p class="u-text -truncate -center -up">
  Hello world, I am awesome, and you probably don't now that
</p>
```

### `u-table`

This makes an element to be represented as a table, which is used to vertically center a content.

```html
<div class="u-table">
  <div class="--inner">
    <img src="pogi.jpg" alt="kier">
    <h1> This should be centered </h1>
  </div>
</div>
```

### `u-clearfix`

This implements the [clearfix hack](http://nicolasgallagher.com/micro-clearfix-hack/) by Nicolas Gallagher which *contains* `floats` withour resorting to representational markup.

By "representational markup", we meant this:

```html
<div style="float: left;"> Sidebar </div>
<div style="float: left;"> Main </div>

<!-- used to contain the two above -->
<div style="clear: both;"></div>

<div> Footer </div>
```

Usage:

```html
<div class="u-clearfix">
  <div class="--left"> Sidebar </div>
  <div class="--right"> Whatebar </div> <!-- pun :> -->
</div>
```

[Back to list](../readme.md#contents)
