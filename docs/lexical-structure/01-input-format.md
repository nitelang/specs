---
icon: lucide/text-initial
---

# Input format
Each source file is interpreted as a sequence of Unicode characters encoded in UTF-8.

!!! Info
    The order in which files are passed to the compiler is not important. Though, passing the same file multiple times is treated as an error.

## Special-character behaviour
Any usage of control characters within source code is permitted, except for **Carriage return (U+000D)** and **Line feed (U+000A)**.
Usage of the **Null (U+0000)** character is forbidden by the standard. The compiler behaviour is undefined.

## Line endings
The language treats invisible line endings characters as trivia, except for [multiline string literals](02-tokens.md).