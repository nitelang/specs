# Expressions

## Precedence

The operations precedence and expressions is ordered as follows, going from strong to weak. Binary Operators at the same precedence level are grouped in the order given by their associativity.

|Expression type|Associativity|
|:--------------|:------------|
|Name||
|Unary `+`, `-`, `&`, `*`||
|`as`||
|`*`, `/`, `%`|Left|
|`+`, `-`|Left|
|`>>`, `>>>`, `<<`|Left|
|`&`|Left|
|`^`|Left|
|`|`|Left|
|`==`, `!=`, `>`, `<`, `>=`, `<=`|Left|
|`&&`|Left|
|`||`|Left|
|`..`|Not allowed together[^1]|
|`..=`|Not allowed together[^1]|
|`=`, `+=`, `-=`,<br/> `*=`, `/=`, `%=`,<br/> `>>=`, `>>>=`, `<<=`,<br/> `&=`, `^=`, `|=`|Right|

[^1]: Syntax `x..y..z` will cause an error, you need to put parentheses to explicitly define associativity.