# JavaScript Loose Equality and Null Handling Bug

This repository demonstrates a common, yet subtle, bug in JavaScript related to the loose equality operator (`==`) and the handling of `null` values. The bug is that the function `foo` unexpectedly returns `null` even when only one of the arguments is `null`, rather than coercing that argument to 0 before addition.

## Bug Description
The JavaScript code contains a function that adds two numbers.  It correctly handles cases where both inputs are numbers. However, when either (or both) input is `null`, it returns `null` instead of performing type coercion (treating `null` as 0).  This is due to the use of loose equality (`===`), which doesn't perform type coercion. 

## Solution
The solution is to use strict equality (`===`) or to explicitly check for null values and handle type coercion before performing the addition operation. 