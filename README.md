# Fenny
A static super tiny language.

```ebnf
File         ::= { FieldPair }

Struct       ::= "{", [FieldPair, {",", FieldPair}, [","]], "}"

FieldPair    ::= [FieldName, "="], Expr

Expr         ::= BinaryExpr

BinaryExpr   ::= UnaryExpr, {BinOp, UnaryExpr}

UnaryExpr    ::= {UnOp}, PostfixExpr

PostfixExpr  ::= Primary, {"(", [Expr, {",", Expr}], ")"}

Primary      ::= Value | "(", Expr, ")"

Value        ::= Struct | Number | String | Bool
```