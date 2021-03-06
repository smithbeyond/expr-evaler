# Expr Evaler(EE)
EE is used to evaluate a bool expr, and get its result(true/false);

In EE's exprs, you can use:

+ <b>predefined</b> variable, but add variables' type must be float64;
+ numbers(float64), '+', '-', '*', '/', '(', ')' to do calculations;
+ '>', '<', '==', '>=', '<=', 'and', 'or' to do logical operations;

# Examples
## Simple Expr
```
Eval("2 * 2*2*2 > 17", nil)

Eval("2+3*5 < (2+3)*5", nil)

Eval("3*3*3 == 27", nil)

Eval("333*3 > 0 and 123 * 0 == 0 and 2 >= 1", nil)

Eval("-23 * -10 == 230", nil)

Eval("-2*-2*-2*-2*-2 == -32", nil)
```

## With Variables
```
Eval("a > b", VarTable{
	"a": 2.2222,
	"b": 034,
})

Eval("a + 34 > b", VarTable{
    "a": 0.2222,
	"b": 034,
})
```

## More Examples
Please see ee_test.go :)