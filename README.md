# AreYouSure.js

Inline confirmation dialogs for Javascript.

[Download](https://raw.github.com/sloria/AreYouSure.js/master/areyousure.js) (3 Kb) [Minified](https://raw.github.com/sloria/AreYouSure.js/master/areyousure.min.js) (2 Kb)

## Demo

http://www.stevenloria.com/AreYouSure.js/

## Usage

```html
<button data-areyousure>Big Red Button</button>
```

That's it!

## And more

Implicit creation using HTML:

```html
<!-- No configuration -->
<button data-areyousure>Default</button>
<!-- Custom text -->
<button data-areyousure="¿Está seguro?" data-confirm="Sí" data-cancel="No">Custom Text</button>
<!-- Callbacks -->
<button id="callbacks" data-areyousure>Callbacks</button>
<script>
$(function() {
    $("#callbacks + .areyousure [data-ays-action='confirm']").on('click', function() {alert("Sure.");});
    $("#callbacks + .areyousure [data-ays-action='cancel']").on('click', function() {alert("Not sure.");});
});
</script>
```

Or programatically, with jQuery:

```javascript
// No configuration
$("#default").areyousure();
// Custom text
$("#customText").areyousure({text: "¿Está seguro?", confirmText: "Sí", cancelText: "No"});
// Callbacks
$("#callback").areyousure({ yes: function() {alert('Sure.');},
                            no:  function() {alert('Not sure.');} });
```

## License

[MIT Licensed](http://sloria.mit-license.org/).



