Lunr Norwegian
==============

This project features a Norwegian trimmer, language stemmer and stopword filter
for [Lunr](http://lunrjs.com/) (a js full text search engine).


# How to use
Lunr-no supports AMD and CommonJS. Check out the examples below:


## In a web browser
Add the following JS files to the page:

```html
<script src="lunr.stemmer.support.js"></script>
<script src="lunr.no.js"></script>
```

then, use the language in when initializing lunr:

```javascript
var index = lunr(function () {
    // use the language
    this.use(lunr.no);
    // then, the normal lunr index initialization
    this.field('title', { boost: 10 });
    this.field('body');
});
```

That's it. Just add the documents and you're done.


## In a web browser, with browserify
**TODO**


## With node.js

```javascript
var lunr = require('lunr');
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
See [lunr-languages](https://github.com/MihaiValentin/lunr-languages#building-your-own-files).


# Technical details & Credits
This is a fork of [lunr-languages](https://github.com/MihaiValentin/lunr-languages).
The code is identical, except an added trimmer.
