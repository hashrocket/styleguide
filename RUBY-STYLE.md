# Ruby Style Guide

You may not like all rules presented here, but they work very well for
us and have helped producing high quality code. Everyone is free to
code however they want, write and follow their own style guides, but
when you contribute to our code, please follow these rules:

## Formatting

* Use ASCII (or UTF-8, if you have to).

* Use 2 space indent, no tabs.

* Use Unix-style line endings.

* Use spaces around operators, after commas, colons and semicolons,
  around `{` and before `}`.

* No spaces after `(` and before `)`.

* Use spaces after `[` and before `]` when defining a new `Array`.

* No spaces after `[` and before `]` when retrieving values from `Array` or `Hash`.

* Use one space before statement modifiers (postfix
  `if`/`unless`/`while`/`until`/`rescue`).

* Indent `private`/`protected` as deep as public method definitions.

* Indent `def`s in `private`/`protected` as deep as public method definitions.

* Use an empty line before and after `private`/`protected`.

* Indent `when` as deep as case.

* Use an empty line between `def`s.

* Use empty lines to break up a long method into logical paragraphs.

* Keep lines fewer than 120 characters.

* Avoid trailing whitespace.

* Ruby file should always end with a newline.

## Syntax

* Use `def` with parentheses when there are arguments.

* Never use `for`, unless you exactly know why.

* Use `&&`/`||` for boolean expressions, `and`/`or` for control flow.

* Avoid multiline `?:`, use `if`.

* Suppress superfluous parentheses when calling methods, but keep them
  when calling "functions", i.e. when you use the return value in the
  same line.

        x = Math.sin(y)
        puts x

* Prefer `{...}` over `do...end`. Use `do...end` for multiline blocks.
  Use `do...end` for "control flow" and "method definitions"
  (e.g. in Rakefiles and certain DSLs.) Avoid `do...end` when chaining.

* Avoid `return` where not required.

* Using the return value of `=` is okay:

        if v = array.grep(/foo/) ...

* Use `||=` freely.

* Use non-OO regexps `=~`, `$0`-`$9`, `$~`, ``$` `` and `$'` when needed.

## Naming

* Use snake_case for methods.

* Use CamelCase for classes and modules. (Keep acronyms like HTTP,
  RFC, XML uppercase.)

* Use SCREAMING_SNAKE_CASE for other constants.

* The length of an identifier determines its scope. Use one-letter
  variables for short block/method parameters, according to this
  scheme:

  * a,b,c: any object
  * d: directory names
  * e: elements of an Enumerable
  * ex: rescued exceptions
  * f: files and file names
  * i,j: indexes
  * k: the key part of a hash entry
  * m: methods
  * o: any object
  * r: return values of short methods
  * s: strings
  * v: any value
  * v: the value part of a hash entry
  * x,y,z: numbers

  And in general, the first letter of the class name if all objects
  are of that type.

* Use _ or names prefixed with _ for unused variables.

* When using inject with short blocks, name the arguments `|a, e|`
  (mnemonic: accumulator, element)

* When defining binary operators, name the argument "other".

* Prefer `map` over `collect`, `detect` over `find`, `select` over `find_all`,
  `size` over `length`.

## Comments

* Use RDoc and its conventions for API documentation. Don't put an
  empty line between the comment block and the `def`.

* Comments longer than a word are capitalized and use punctuation.
  Use one space after periods.

* Use one space after `#`:

        # This is my comment.

* Avoid superfluous comments.

* Do not prefix the comments with your nickname.

## The rest

* Write `ruby -w` safe code.

* Avoid hashes-as-optional-parameters. Does the method do too much?

* Avoid long methods.

* Avoid long parameter lists.

* Use `def self.method` to define singleton methods.

* Add "global" methods to `Kernel` (if you have to) and make them private.

* Use `OptionParser` for parsing complex command line options and
  `ruby -s` for trivial command line options.

* Write for 1.8, but avoid doing things you know that will break in 1.9.

* Avoid needless metaprogramming.

## General

* Every lib or project should have [README.md](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html) file

* Code in a functional way, avoid mutation when it makes sense.

* Do not mutate arguments unless that is the purpose of the method
  (use `!` suffix for those methods).

* Do not mess around in core classes when writing libraries.

* Do not program defensively.
  (See http://www.erlang.se/doc/programming_rules.shtml#HDR11.)

* Keep the code simple.

* Don't overdesign.

* Don't underdesign.

* Avoid bugs.

* Read other style guides and apply the parts that don't dissent with
  this list.

* Be consistent.

* Use common sense.
