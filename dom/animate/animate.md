@page jQuery.animate
@parent jquerypp

`jQuery.animate` overwrites `[jQuery.fn.animate jQuery.fn.animate(properties, duration, callback)]`
and enables it to animate properties using CSS 3 animations, if supported.
If the browser doesn't support CSS animations, the original
[jQuery.fn.animate()](http://api.jquery.com/animate/) will be used.

## Compatibility

`jQuery.fn.animate` is mostly compatible with the original [jQuery.fn.animate()](http://api.jquery.com/animate/)
which will be used as a fallback when

- The browser doesn't support CSS animations (checked with `window.WebKitAnimationEvent`)
- The duration is not a number
- A property is set to `show` or `hide` which is used by jQuery to set the original property
- The properties are empty
- The elements are not DOM nodes (e.g. created with `$({ test : 'object' })`)
- The element is displayed `inline`

## Example

The following example creates a fade-in effect using CSS animations:

    $('#element').css({
      opacity : 0
    }).anifast({
      opacity : 1
    }, 1000, function() {
      console.log('Animation done');
    });

## Demo

The following demo is based on the [jQuery .animate reference](http://api.jquery.com/animate/) but uses CSS animations:

@demo jquery/dom/animate/animate.html 400