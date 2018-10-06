
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

## Cost
 - For W3C browsers: ~8KiB gziped

## Installation
  Add main script in `head` section
  
            <script src="a.js"></script>

## EXSTRAS

(pseudocode)

IF \_\_GCC\_\_INCLUDE\_EXTRAS\_\_ == false -> Broken Object.defineProperty and Object.defineProperties will be deleted

IF \_\_GCC\_\_INCLUDE\_EXTRAS\_\_ == true ->

 - Exporting these objects to global (window)
	1. browser
	2. DOMStringCollection
	3. XHR from https://github.com/Raynos/xhr with customisations
 - Extending objects
	1. Object.append(object, donor, [donor2, ...])
	2. Object.extend(object, donor, [donor2, ...]) (Object.append with overwrite exists properties)
	3. Object.inherits(Child, Parent)
	4. Array.prototype.unique()
	5. String.random(length)

Note: if you don't need Extras set [GCC](https://developers.google.com/closure/compiler/) flag **\_\_GCC\_\_INCLUDE\_EXTRAS\_\_** to **false** in a.js and recompile a.js using [Google Closure Compiler](closure-compiler.appspot.com/home) \([GCC online](closure-compiler.appspot.com/home)\)

## Customisation
In addition to **\_\_GCC\_\_INCLUDE\_EXTRAS\_\_** [GCC](https://developers.google.com/closure/compiler/) flag there are a bunch of over flags to enable/disable ES5/6 and DOM3/4 shims in a.js file. After set flags you need to recompile a.js using [Google Closure Compiler](closure-compiler.appspot.com/home) \([GCC online](closure-compiler.appspot.com/home)\)

## DEBUG

If [GCC](https://developers.google.com/closure/compiler/) flag **\_\_GCC\_\_IS\_DEBUG\_\_** == **true** -> Console fix from https://github.com/theshock/console-cap/blob/master/console.js
 

## Known issues:
0. Lack of test cases

## TODO
1. Tests

## License

    MIT
