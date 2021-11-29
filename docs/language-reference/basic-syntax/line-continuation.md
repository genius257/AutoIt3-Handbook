# Line continuation

Although only one statement per line is allowed, a long statement can span multiple lines if an underscore " _" preceded by a blank is placed at the end of a "broken" line. String definition cannot be split in several lines, concatenation need to be used.

```autoit
#include <MsgBoxConstants.au3>

MsgBox($MB_SYSTEMMODAL, "", "This is a rather long line, so I " & _
        "broke it with the underscore, _, character.") 
```
