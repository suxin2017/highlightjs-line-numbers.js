# highlightjs-line-numbers.js [![npm](https://img.shields.io/npm/v/highlightjs-line-numbers.js.svg)](https://www.npmjs.com/package/highlightjs-line-numbers.js) ![npm](https://img.shields.io/npm/dw/highlightjs-line-numbers.js.svg)

Highlight.js line numbers plugin.

[DEMO](http://wcoder.github.io/highlightjs-line-numbers.js/) | [SСREENSHOTS](https://github.com/wcoder/highlightjs-line-numbers.js/issues/5)

## Install

#### Bower
```
bower install highlightjs-line-numbers.js
```

#### Npm
```
npm install highlightjs-line-numbers.js
```

#### Getting the library from CDN
```html
<script src="//cdnjs.cloudflare.com/ajax/libs/highlightjs-line-numbers.js/2.6.0/highlightjs-line-numbers.min.js"></script>
```
```html
<script src="//cdn.jsdelivr.net/npm/highlightjs-line-numbers.js@2.6.0/dist/highlightjs-line-numbers.min.js"></script>
```

## Usage

Download plugin and include file after highlight.js:
```html
<script src="path/to/highlight.min.js"></script>

<script src="path/to/highlightjs-line-numbers.min.js"></script>
```

Initialize plugin after highlight.js:
```js
hljs.initHighlightingOnLoad();

hljs.initLineNumbersOnLoad();
```

Here’s an equivalent way to calling `initLineNumbersOnLoad` using jQuery:
```js
$(document).ready(function() {
    $('code.hljs').each(function(i, block) {
        hljs.lineNumbersBlock(block);
    });
});
```

If your needs cool style, add styles by taste:
```css
/* for block of numbers */
.hljs-ln td.hljs-ln-numbers {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;

    text-align: center;
    color: #ccc;
    border-right: 1px solid #CCC;
    vertical-align: top;
    padding-right: 5px;

    /* your custom style here */
}

/* for block of code */
.hljs-ln td.hljs-ln-code {
    padding-left: 10px;
}
```

## Options

After version 2.1 plugin has optional parameter `options` - for custom setup.

name       | type    | default value | description
-----------|---------|---------------|-----------------------
singleLine | boolean | false         | enable plugin for code block with one line

#### Examples of using

```js
hljs.initLineNumbersOnLoad({
    singleLine: true
});
```

```js
hljs.lineNumbersBlock(myCodeBlock, myOptions);
```

---
&copy; 2018 Yauheni Pakala | MIT License
