SASS-Toolshed
=============

Everyday mixins for SASS. Use `@import 'toolshed'` to use.

You may also want to use Compass (http://compass-style.org/).

How to work with sprites
------------------------

```scss
// $name    (string)  name of icon
// $yOffset (integer) variant of said icon
// $mode    (integer)
@mixin base-icon-sprite($name, $yOffset : 0, $mode : 0) {
	$width-sprite: 1200px;
	$height-sprite: 1200px;

	$xOffset: 0;

	$iconWidth: 22px;
	$iconHeight: $iconWidth;

	@if ($name == "logo-big") {
		$xOffset: 0;
		$iconWidth: 105px;
		$iconHeight: 115px;
	} @else if ($name == "arrow-up-white") {
		$xOffset: 1;
	} @else if ($name == "arrow-up-green") {
		$xOffset: 2;
	} @else if ($name == "angle-down") {
		$xOffset: 3;
	} @else if ($name == "angle-up") {
		$xOffset: 4;
	} @else if ($name == "angle-left-big") {
		$xOffset: 5;
	} @else if ($name == "angle-right-big") {
		$xOffset: 6;
	} @else if ($name == "angle-down-big") {
		$xOffset: 7;
		$iconWidth: 34px;
		$iconHeight: $iconWidth;
	} @else if ($name == "map-marker") {
		$xOffset: 8;
		$iconWidth: 24px;
		$iconHeight: 34px;
	} @else if ($name == "logo") {
		$xOffset: 9;
		$iconWidth: 62px;
		$iconHeight: 26px;
	}

	@include toolshed-grid-sprite-complete (
		"../img/shi-basics.png",
		"../img/shi-basics@2x.png",
		1200px,
		360px,
		120px,
		120px,
		$iconWidth,
		$iconHeight,
		$xOffset,
		$yOffset,
		$mode
	);
}
```

Version
-------

Version: 1.2 (2014-07-25)

Legal stuff
-----------

Author: [Frank Boës](http://3960.org)

Copyright & license: See LICENSE.txt