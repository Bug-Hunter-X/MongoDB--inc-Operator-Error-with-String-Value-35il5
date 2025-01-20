# MongoDB $inc Operator Error with String Value

This repository demonstrates an uncommon error related to the usage of the `$inc` operator in MongoDB's `findOneAndUpdate` method.

The error occurs when attempting to increment a field with a string value instead of a number. This leads to the field not being updated correctly or unpredictable results.

## Bug Description
The `$inc` operator is designed to increment numerical values. Providing a string value will not produce the expected result. This might result in data corruption if not properly handled.

## Solution
The solution involves ensuring the value passed to the `$inc` operator is a number. This requires verifying data types before updating the document.