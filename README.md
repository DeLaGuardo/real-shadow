# [Real Shadow](http://indamix.github.com/real-shadow/) - jQuery Plugin that casts photorealistic shadows
Perfect for eye-catching demos and landing pages.

Works in any browser supporting CSS box-shadow property.

## What's new in v1.1.0
+ possibility to update shadows during/after jQuery animations
+ inset shadows
+ optimizations
+ corrected shadow positions

## Basic Usage

```javascript
$(selector).realshadow(); // options are optional

$(selector).realshadow({

	followMouse: false,   // true by default

	pageX:       x,       // x coordinate of the light source
	pageY:       y        // y coordinate of the light source

	c: {                  // shadow color
		r: 1,             // red   channel for shadow
		g: 1,             // green channel for shadow
		b: 1,             // blue  channel for shadow
	}

});
```

To specify different colors for each element, you can use "rel" attribute:

```html
<span rel="r"></span>
<span rel="g"></span>
<span rel="b"></span>
<span rel="rg"></span>
<span rel="gb"></span>
<span rel="br"></span>
<span rel="rgb"></span>
```

```javascript
$('span').realshadow();
```

## Inset Shadows

```javascript
$(selector).realshadow({
	inset: true
});
```

### Update shadows during/after jQuery animations
```javascript
	// before: apply Real Shadow to elements:
	$(selector).realshadow(/* options, if needed */);

	// update shadows during jQuery animation, i.e. each animation step:
	$(selector).animate(/* animated properties */, {step: $.fn.realshadow.update});

	// update shadows after jQuery animation is over:
	$(selector).animate(/* animated properties */, $.fn.realshadow.update);
```
If you update shadows during jQuery animation, you don't need to update shadows after jQuery animation is over.


If you suppose that the usage of Real Shadow is unclear, feel free to contact me.