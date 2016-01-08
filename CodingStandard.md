# Coding Style Guidelines #

## Formatting ##
In general, we use the code formatting options provided by Visual Studio 2010's "Visual C#" default configuration, with one exception:
  * Format with tabs, not spaces.

Additionally, we use the following rules:
  * Each statement should get its own line.
  * Braces should be omitted when possible.
  * However, braces should only be omitted for complex control constructs (`if`/`else`, `try`/`catch`) if they can be omitted for all blocks in the construct.
  * Access modifiers should be omitted when possible.
  * Although this should be used judiciously, calls to functions with long or complex parameter lists should be indented using K&R style for the parentheses, and this technique should be nested as appropriate:
```
PerformComplexOperation(
  argument1,
  someValue ? option1 : option2,
  SomeOtherFunction(
    a,
    b,
    c
  ),
  lastValue
)
```

## Style ##
  * Use the .NET guidelines unless they conflict with something on this page.
  * Use `var` when possible.
  * Do not created nested types.

## Naming ##
  1. Identifiers should be named in such a way as to clearly illustrate their purpose or meaning. Abbreviations should be avoided.
  1. PascalCase should be used for types, methods and properties. camelCase should be used for variables and fields.
  1. All letters of an acronym should be capitalized, except with the acronym is the first word of a camelCase identifier, in which case all letters should be lowercase.
  1. Boolean properties should begin with a word that suggests their boolean nature, such as "is."
  1. Do not decorate field names with prefixes (for example, with `m`).
  1. Do not decorate type names with prefixes (for example, with `I`).
  1. In declarations, the access modifier (if applicable) should precede the static/virtual/et cetera designator.

## Commenting ##
Comment intelligently; don't comment code that is otherwise readable and self-documenting. Instead, prefer to comment only where value would be added, such as by explaining why a particular implementation was made in favor of another that might be more obvious or standard.

  1. C-style comments should be avoided.
  1. There should be a single blank line between the last line of a file header copyright and the first line of code.
  1. Comments should not be placed on the same line as code statements.
  1. Insert a space between the comment delimiter and the first character of the comment.
  1. XML documentation comments should be added to every non-private item.
  1. Prefer to avoid committing large blocks of commented-out code. That's what version control is for.