# noUiSlider

noUiSlider is lightweight JavaScript range slider, originally developed to be a jQuery UI alternative.

It features cross-browser support, a wide range of options and support for a bunch of touch devices. It has been tested on Android phones, iPhone & iPad, Windows phone and touch-screen laptops and tablets and desktops.

All modern browsers and [IE9+](#browser-support) are supported. noUiSlider has no dependencies, and is licensed [WTFPL](http://www.wtfpl.net/about/).

Documentation
-------
An extensive documentation, including **examples**, **options** and **configuration details**, is available here: [noUiSlider documentation](https://refreshless.com/nouislider/).

Changelog
---------
### 9.0.0
- Added: Support for **more than 2 handles**;
- Added: `format` option can be updated (#641);
- Added: `reset` method the return slider to start values (#673);
- Change: `connect` option is now implemented as a separate node;
- Change: all event arguments, including the handle number, are now in slider order;
- Change: `updateOptions` now **modifies the original options** object. The reference in `slider.noUiSlider.options` remains up to date (#678);
- Change: more events fire when using various `behaviour` options (#664);
- Change: on `rtl` sliders, handles are now visually positioned from the sliders `right`/`bottom` edge;
- Change: events for `rtl` sliders now fire in the same order has for `ltr` sliders (with incremental handleNumbers);
- Change: internal `Spectrum` component is no longer `direction` aware;
- Change: `limit` and `margin` must be divisible by `step` (if set);
- Removed: `.noUi-stacking` class. Handles now stack themselves;
- Removed: `.noUi-handle-lower` and `.noUi-handle-upper` classes;
- Removed: `.noUi-background`. This is now default;
- Removed: `connect: 'lower'` and `connect: 'upper'`. These settings are replaced by `connect: [true, false]`;
- Fixed: default tooltip color (#687);
- Fixed: `margin` and `limit` calculated improperly after calling `updateOptions` with a new `range` option;
- Fixed: `range` option was required in update, even when not updating it (#682);
- Fixed: Cursor styling is now consistent for disable handles and sliders (#644);

Devices
-------
Devices/browsers tested:
- Surface Pro 3 (Windows 10)
- iPad Air 2 (iOS 9.3)
- iPad 3 (iOS 8.4)
- Moto E (Android 5.1, Chrome)
- Lumia 930 (WP8.1, IE10 mobile)
- Lumia 930 (WM10, Edge)
- Asus S400C (Windows 10, Touch + mouse)
	+ Chrome
	+ Firefox
	+ Edge
	+ IE11
	+ IE10 (Emulated)
	+ IE9 (Emulated)

Bower
-----
Bower users can install all compiled and minified files easily using `bower install nouislider --save`. Supporting bower unfortunately means keeping all compiled and minified versions in the repository.

Browserify
----------
This library is [UMD](https://github.com/umdjs/umd) compatible, so you can use it in this way:

```javascript
var noUiSlider = require('nouislider');

var slider = document.getElementById('slider');

noUiSlider.create(slider, {
  start: 40,
  connect: "lower",
  range: {
    min: 0,
    max: 100
  }
});
```

Browser support
---------------

All major browsers are supported. **To support IE8** you'll need to shim several ES5 features.

You can use [polyfill.io](https://cdn.polyfill.io/v2/docs/) to easily do so:

```html
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
<!--[if lte IE 8]>
<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>
<![endif]-->
```

Version numbering
------------------------------
Version numbering follows the 'Semantic versioning' style.
You'll find an excellent documentation at [Semver.org](http://semver.org/).
