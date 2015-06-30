Norwegian lunr
==============

[lunr-no](https://github.com/arve0/lunr-no) features a Norwegian trimmer,
language stemmer and stopword filter for [Lunr.js](http://lunrjs.com/) (a js
full text search engine).


# How to use
lunr-no supports AMD and CommonJS. Check out the examples below:


## In a web browser
Add the following JS files to the page:

```html
<script src="lunr.stemmer.support.js"></script>
<script src="lunr.no.js"></script>
```

then, use the language in when initializing lunr:

```js
var index = lunr(function () {
    // use the language
    this.use(lunr.no);
    // then, the normal lunr index initialization
    this.field('title', { boost: 10 });
    this.field('body');
});
```

That's it. Just add the documents and you're done.


## With node.js (or with browserify)

```js
var lunr = require('lunr');
require('lunr-no/lunr.stemmer.support.js')(lunr);
require('lunr-no')(lunr);

var index = lunr(function () {
    // use the language
    this.use(lunr.no);
    // then, the normal lunr index initialization
    this.field('title', { boost: 10 })
    this.field('body')
});
```


# Building your own files
See [lunr-languages][build].

[build]: https://github.com/MihaiValentin/lunr-languages#building-your-own-files


# Technical details & Credits
This is a fork of [lunr-languages](https://github.com/MihaiValentin/lunr-languages).
The code is identical, except the added trimmer.
