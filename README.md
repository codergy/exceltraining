# Basic Excel training
Basic Excel training for co-workers - DRAFT

## Table of Contents

1. Vlookup
1. If and nested if
1. String-related formulas
1. Counting

## Common VLOOKUP problems

## Logical functions
### IF()
*=IF(logical_test; [value_if_true]; [value_if_false])*

    =IF(A1 > B1; "A1 is greater than B1"; "A1 is equal or less than B1")
### Nested IF()
*IF (logical_test;* IF(logical_test; [value_if_true]; [value_if_false])*; [value_if_false])*

    =IF(A1>=B1;IF(A1=B1;"A1 is equal to B1";"A1 is greater than B1");"A1 is less than B1")
### AND()
The [AND function](https://exceljet.net/excel-functions/excel-and-function) is a logical function used to require more than one condition at the same time. AND returns either TRUE or FALSE.

*=AND (logical1; [logical2]; ...)*

    =IF(AND(A1>B1;C1>E1);"A1 is greater than B1, and C1 is greater than E1";"Either A1 or C1 is less or equal to B1 and E1, respectively.")
### OR()
The [OR function](https://exceljet.net/excel-functions/excel-or-function) is a logical function to test multiple conditions at the same time. OR returns either TRUE or FALSE. The return value is TRUE if any arguments evaluate TRUE; FALSE if not.

*=OR (logical1; [logical2]; ...)*

    =IF(OR(A1>B1;C1>E1);"Either A1 is greater than B1, or C1 is greater than E1, or both are greater than their pairs";"Both A1 or C1 are less or equal to B1 and E1, respectively.")
### NOT()
The Excel [NOT function](https://exceljet.net/excel-functions/excel-not-function) returns the opposite of a given logical or boolean value. When given TRUE, NOT returns FALSE. When given FALSE, NOT returns TRUE. Use the NOT function to reverse a logical value.

*=NOT (logical)*

    =IF(NOT(A1=B1);"A1 is not equal to B1";"A1 is equal to B1")
### Nested logical operators

![Nested logical operators](nested_logical.png?raw=true "Nested logical operators")

    =IF(NOT(AND(A1=B1;C1=D1));"OK";"Not OK")
1. A1=B1 evaluates to **TRUE**, because 1=1
1. C1=D1 evaluates to **FALSE**, because 2<>3
1. AND(A1=B1;C1=D1) evaluates to **FALSE**, because not all parameters evaluates to **TRUE**.
1. NOT(AND(A1=B1;C1=D1)) evaluates to **TRUE**, because it negates the **FALSE** evaluation of AND(...).

**To sum it up:** NOT(AND(TRUE;FALSE)) = NOT(FALSE) = TRUE

### IFERROR()

## Text functions
### TRIM()
### LEN()
### LEFT(), RIGHT()
### MID()
### TEXT()

## Statistical functions
### COUNT
### COUNTIF
### SUMIF

## Mathematic formulas
### AVERAGE()
### MIN(), MAX()
### ABS()
### ROUND()

## Time functions
### NOW()
### TIME()
