# Strings

## String escape
AutoIt3 does not have string escape, except with the initial string quote char.
To do this, simply add two of the same quote to escape the quotation char.
Example:

```AutoIt3
ConsoleWrite("a""b" & 'c''d') ; a"bc'd
```
