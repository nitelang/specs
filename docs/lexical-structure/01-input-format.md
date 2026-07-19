---
icon: lucide/text-initial
---

# Input format
Each source file is interpreted as a sequence of Unicode characters encoded in UTF-8.

!!! Info
    The passing file order to the compiler is not important. Though, passing same file multiple times is treated as error.

## Special-character behaviour
Any usage of control characters within source code is permitted, except for **Carriage return (U+000D)** and **Line feed (U+000A)**.
Usage of the **Null (U+0000)** character is forbidden in standard. The compiler behaviour is undetermined.

## Line endings
Language treats invisible line endings characters as trivia, except for [multiline string literals](02-tokens.md).