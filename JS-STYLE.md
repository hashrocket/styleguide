# JavaScript Style Guide

You may not like all rules presented here, but they work very well for
us and have helped producing high quality code. Everyone is free to
code however they want, write and follow their own style guides, but
when you contribute to our code, please follow these rules:

## Formatting

* Use ASCII (or UTF-8, if you have to).

* Use 2 space indent, no tabs.

* Use Unix-style line endings.

* Use spaces after `{` and before `}`.

* Use space after `:` when defining objects.

        { a: 1, b: 2 }

* No spaces after `(` and before `)`.

* Use spaces after `[` and before `]` when defining a new `Array`.

* No spaces after `[` and before `]` when retrieving values from `Array` or `Object`.

* No space before `(` in function definitions.

        function() { ... }
        function abc() { ... }

* Use space after `if`/`while`/`for`/`switch`.

        if (true) { ... }

* Use empty lines to break up a long function into logical paragraphs.

* Keep lines fewer than 120 characters.

* Avoid trailing whitespace.

* JavaScript file should always end with a newline.

## Syntax

* Always declare local variables with `var`.

* Always use `{` and `}` in control flows.

        if (true) {
          return true;
        } else {
          return false;
        }

## Naming

* Use camelCase for variables and functions.

* Prefix jQuery objects with `$`:

        var $links = $('a');

## General

* Use common sense.
