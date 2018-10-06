
# ES5 and DOM4 shim for all browsers
based on:

- https://github.com/kriskowal/es5-shim
- https://github.com/paulmillr/es6-shim
- https://github.com/Raynos/DOM-shim

__Status__: Stable Beta

## Goal

 - Normalizing the JS and DOM across all browsers
 - Less code (eg less closures, reusable functions) & file size
 - Include all we need from ES5, ES6 and DOM shim in one file
 - Powerful customisation

## Brief

 - Add methods such [add/remove]EventListener, querySelector[All], setSelectionRange
 - Add Element/Node properties such classList, children, [first/last]ElementChild, reversed, control, labels
 - Add methods such insertAdjacentHTML (old FF), stopImmediatePropagation  (Opera < 12) and properties reversed, control, labels, etc in W3C browsers
 - Add ES5/6 methods in all browsers
 - Add DOM4 methods append, prepend, after, before, replace, remove, match in all browsers
 - Provide bugs fixing for DOM and ES in Opera, Chrome, FF
 - and more

## Installation
  Add main script in `head` section
  
            <script src="a.js"></script>

## TODO
1. Tests

## License

    MIT
