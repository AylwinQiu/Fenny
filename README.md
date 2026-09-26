# Fenny
A static super tiny language.

```ebnf
file ::= FieldPair;
Struct ::= `{` {FieldPair} `}`
FieldPair ::= [FieldName, `=`], Expr, `,`;
Expr ::= Value | Proc
Value ::= Struct | Number | String | Bool
Proc ::= 
```