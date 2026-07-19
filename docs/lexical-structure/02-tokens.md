---
icon: lucide/braces
---


# Tokens
During lexical analysis source file text is separated into distinctive meaningful tokens.

Each source contains at least one *end-of-file* token.

## Identifiers
The primary purpose of identifiers is to give a human-readable name to the specific program part.

```ebnf
identifier = identifier_or_keyword | escaped_identifier ;
```

### Regular identifier

A regular identifier begins with a letter or underscore and is followed by any number of letters, digits, underscores, or marks.

```ebnf
identifier_or_keyword = identifier_start { identifier_continue } ;

identifier_start      = "_" | letter ;
identifier_continue   = "_" | letter | digit ;

letter = <Lu> | <Ll> | <Lt> | <Lm> | <Lo> | <Nl> ; (* (1)! *)
digit  = "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9" ;
```

1. Wikipedia page about unicode categories:  
   https://en.wikipedia.org/wiki/Unicode_character_property#General_Category

!!! Note
    As you can see: the identifier support not only ASCII letters, but the whole letter unicode category.
    This means you can use your native language for identifier, for example `привет_мир` is a valid identifier.

### Escaped identifier
An escaped identifier is enclosed in backtick characters and may contain any character, including those that are otherwise invalid in identifiers. Escape sequences are supported inside escaped identifiers.

```ebnf
escaped_identifier =
    "`" { escaped_identifier_character | escape_sequence } "`" ;

escaped_identifier_character =
    ? any Unicode scalar value except LF, CR, "\", and "`" ? ;

escape_sequence =
      "\\"
    | "\`"
    | "\a"
    | "\b"
    | "\f"
    | "\n"
    | "\r"
    | "\t"
    | "\v"
    | "\0"
    | "\u" hex_digit hex_digit hex_digit hex_digit
    | "\U" hex_digit hex_digit hex_digit hex_digit
           hex_digit hex_digit hex_digit hex_digit
    ;

hex_digit =
      digit
    | "A" | "B" | "C" | "D" | "E" | "F"
    | "a" | "b" | "c" | "d" | "e" | "f" ;
```

## Punctuators and operators
|Preview|Name|Description|
|------:|:---|:----------|
|`.`|Dot|
|`,`|Comma|
|`:`|Colon|
|`->`|Retusa|Defines return type|
|`::`|DoubleColon|Part of the qualified paths|
|`{`|OpenBrace
|`}`|CloseBrace
|`(`|OpenParen
|`)`|CloseParen
|`[`|OpenBracket
|`]`|ClosBracket
|`+`|Plus|
|`+=`|PlusEquals|
|`-`|Minus|
|`-=`|MinusEquals|
|`*`|Asterisk|
|`*=`|AsteriskEquals|
|`/`|Slash|
|`/=`|SlashEquals|
|`%`|Percent|
|`%=`|PercentEuqlas|
|`&`|Ampersand|
|`&=`|AmpersandEquals|
|`&&`|DoubleAmpersand|
|`^`|Caret|
|`^=`|CaretEquals|
|`|`|Bar|
|`|=`|BarEquals|
|`||`|DoubleBar|
|`~`|Tilde|
|`~=`|TildeEquals|
|`!`|Exclamation|
|`..`|Range|
|`..=`|InclusiveRange|
|`>>`|RightShift[^1]|
|`>>=`|RightShiftEquals|
|`>>>`|UnsignedRightShift[^1]|
|`>>>=`|UnsignedRightShiftEquals|
|`<<`|LeftShift|
|`<<=`|LeftShiftEquals|
|`=`|Equals|
|`==`|DoubleEquals|
|`!=`|NotEquals|
|`<`|Less|
|`<=`|LessEquals|
|`>`|Greater|
|`>=`|GreaterEquals|

[^1]: Depending on context right shift operators can be treated as several generic parameter list close tokens.

## Literals
TODO

## Keywords
Keywords is really much identifiers, except they cannot be used as such. They are reserved words language use in different contexts.

### Strong keywords
TODO

### Contextual keywords
TODO

### Reserved keywords
TODO