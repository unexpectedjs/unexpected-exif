---
template: default.ejs
theme: dark
title: unexpected-exif
repository: https://github.com/unexpectedjs/unexpected-exif
---

# unexpected-exif

EXIF data plugin for the [Unexpected](https://unexpected.js.org/) assertion library (version 7+ required). Uses the [exif-parser](https://github.com/bwindels/exif-parser) module to do most of the work.

[![NPM version](https://badge.fury.io/js/unexpected-exif.svg)](http://badge.fury.io/js/unexpected-exif)
[![Build Status](https://travis-ci.org/unexpectedjs/unexpected-exif.svg?branch=master)](https://travis-ci.org/unexpectedjs/unexpected-exif)
[![Coverage Status](https://coveralls.io/repos/unexpectedjs/unexpected-exif/badge.svg)](https://coveralls.io/r/unexpectedjs/unexpected-exif)
[![Dependency Status](https://david-dm.org/unexpectedjs/unexpected-exif.svg)](https://david-dm.org/unexpectedjs/unexpected-exif)

The image can be specified either as a string (file name) or as a Buffer instance.

```js#async:true
return expect('magic-pen-6-colours.jpg', 'to have EXIF data satisfying', {
  tags: {
    XResolution: 72,
    Model: 'iPhone 6',
  },
});
```

```output
expected magic-pen-6-colours.jpg (image/jpeg)
to have EXIF data satisfying { tags: { XResolution: 72, Model: 'iPhone 6' } }

{
  tags: {
    ProcessingSoftware: 'gThumb 3.0.2',
    Orientation: 1,
    XResolution: 72,
    YResolution: 72,
    ResolutionUnit: 2,
    ModifyDate: 1405268464,
    YCbCrPositioning: 1,
    ColorSpace: 1,
    ExifImageWidth: 380,
    ExifImageHeight: 248
    // missing Model: 'iPhone 6'
  },
  imageSize: { height: 248, width: 380 },
  thumbnailOffset: 300,
  thumbnailLength: 2152,
  thumbnailType: 6,
  app1Offset: 24
}
```

Read [the documentation](http://unexpected.js.org/unexpected-exif/).

## Releases

[Changelog](https://github.com/unexpectedjs/unexpected-exif/blob/master/CHANGELOG.md)

## License

Unexpected-exif is licensed under a standard 3-clause BSD license -- see
the `LICENSE` file for details.
