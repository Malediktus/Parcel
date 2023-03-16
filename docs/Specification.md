# Parcel Specification

## General

Parcel is a general purpose open source scripting language. It compiles to a bytecode
format which get stored in a cache directory by a just in time bytecode compiler, similar to Python3.

## Syntax

Each statement should be finished by a semicolon (;). Bodys are started using '{' and should be ended with '}'. A Body can be used to isolate variables because it opens a new
namespace which inherits from it's parent. A function must be defined using the 'function' keyword
follow by a identifier which will be used to call or access this function. This identifier must be unique in the current namespace and it's parents.
If this is not defined a runtime error called 'Identifier Exists Exception' should be thrown. The format for errors whill be defined in the 'Errors' section. A function
declaration must be followed by a statement or a body containing multiple statements.
A function can be ended early by the 'return' keyword followed by a value or nothing.
If it value is specified the function returns this value. A return statement
can also be used to return a value at the end of a function. Variables should be defined
with the 'var' keyword followed by an identifier with the same rules as a function identifier.
After that a '=' is expected followed by a value. Values can be modified with there identifier followed by '=' and they're new value.
Values can be a number. A number can be a float defines with a '.' followed by digits.
Strings should be started and ended with '=' character and they're value in between.
They can contain the following escape sequences: '\"', '\n', '\t', '\r'.