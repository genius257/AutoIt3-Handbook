# Coding Style Conventions

Coding style conventions are used in this sample series to aid clarity and consistency. The "Hungarian" notation conventions are used.  
They include variable prefix notations that give to variable names a suggestion of the type of the variable.

AutoIt3 does have it's own official coding style convention here: [Best coding practices]().  
However it is missing some tings, like a few variable type prefixes and not having guidelines to prevent UDF varaible naming conflicts.  
It is NOT recommended to mix theese coding practices.

This page is based on [MSDN Coding Style Conventions](https://docs.microsoft.com/en-us/windows/win32/stg/coding-style-conventions), modified to AutoIt3 needs.

## Variables

The following table lists common variable prefixes.

| Prefix | Description                         |
| :----- | :---------------------------------- |
| a      | Array                               |
| b      | Boolean                             |
| c      | Char                                |
| cb     | Count of bytes                      |
| cr     | Color reference value               |
| d      | Binary                              |
| db     | Double                              |
| f      | Flags (usually multiple bit values) |
| fn     | Function                            |
| fp     | Floating-point                      |
| g_     | Global                              |
| h      | Handle                              |
| i      | Integer                             |
| m_     | Data member of a class              |
| n      | Number                              |
| o      | Object                              |
| p      | Pointer                             |
| s      | String                              |
| sz     | Zero terminated String              |
| t      | DllStruct                           |
| tag    | DllStruct structure definition      |
| v      | Variant                             |


These are often combined, as in the following.

| Prefix combination | Description                            |
| :----------------- | :------------------------------------- |
| pszMyString        | A pointer to a zero terminated string. |
| asDays             | An array of strings                    |
| anArray            | An array of numbers                    |

## Functions

## DllStruct element names

## UDFs

UDFs should try to follow guidelines below to avoid naming conflicts.

### Variables

Global variables in UDFs should use the prefix: `__g_` followed by the UDF "namespace"  
Example: `$__g_AutoIt3Handbook_sMyString` where `AutoIt3Handbook` reprensents the UDF "namespace"

### Functions

UDF functions should use the prefix `_` followed by the UDF "namespace"  
Example: `_AutoIt3Handbook_MyFunction()` where `AutoIt3Handbook` reprensents the UDF "namespace"
