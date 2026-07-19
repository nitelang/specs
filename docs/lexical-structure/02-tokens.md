---
icon: lucide/braces
---


# Tokens
During lexical analysis source file text is separated into distinctive meaningful tokens.

Each source contains at least one *end-of-file* token.

## Identifiers
TODO

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