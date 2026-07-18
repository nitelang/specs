---
icon: lucide/braces
---


# Tokens
During lexical analysis source file text is separated into distinctive meaningful tokens.

Each source contains at least one *end-of-file* token.

## Punctuators and operators
|Preview|Name|Description|
|------:|:---|:----------|
|`.`|Dot|
|`,`|Comma|
|`:`|Colon|
|`->`|Retusa|Defines return type|
|`::`|DoubleColon|Part of the qualified paths|
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
|`&&`|DoubleAmpersand|
|`&=`|AmpersandEquals|
|`^`|Caret|
|`^=`|CaretEquals|
|`|`|Bar|
|`||`|DoubleBar|
|`|=`|BarEquals|
|`~`|Tilde|
|`~`|TildeEquals|
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

## Keywords

### Type keywords

### Weak keywords

### Strong keywords

### Reserved keywords