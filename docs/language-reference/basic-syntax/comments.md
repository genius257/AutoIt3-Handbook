# Comments

Comments are sections of text within AutoIt3 code that are ignored at runtime.

## Single line comments

Single line comments in AutoIt3 uses a semicolon to indicate the start of the comment and everything preceding the symbol on the same line is ignored by the interpreter. (If not within a string)

```autoit
; This is a stand alone single line comment
MsgBox(0, "Title", "; Message"); This is a single line comment, following a statement
```

Single line comments are also allowed on expressions using [line continuation](./line-continuation.md) like so:

```autoit
MsgBox( _
    "Title" _; This is the title of the message box
    "Message"; This is the message of the message box
)
```

## Multi line comments

Multi line comments uses preprocessor directives to indicate start and stop of the comment block.

Comment blocks must be closed, meaning a comment block without a ending multi line comment directive is not allowed.

`#cs` or `#comments-start` starts a multi line comment and `#ce` or `#comments-end` ends it.

Mixing the type of directives for starting and closing is allowed, meaning you could start a block with `#cs` and end with `#comments-end`.

An important note is that comment rules within multi line comment blocks apply, meaning multiline comments are possible, and single line comments can disable a multi line directive.

```autoit
#cs
    #comments-start
        The line below does not end the nested comment block, due to the preceding semicolon.
        ; #comments-end
    #comments-end

    #cs
        Less readable comment block, but functional.
    #comments-end
#ce
```

## Preprocessor Directives

It is also possible to make comments, using the preprocessor directive line format, however this is not recommended, as certain formatting may collide with the preprocessor in unintended ways.

The preprocessor directive cannot precede code on a line, and everythig preceeding the # symbol on the same line is ignored by the interpreter. (If not within a string)

```autoit
# This is a comment, within a preprocessor directive
MsgBox(0, "Title", "# Message")
```
