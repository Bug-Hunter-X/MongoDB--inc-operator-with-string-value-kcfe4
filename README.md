# MongoDB $inc operator with string value

This example demonstrates an uncommon error in MongoDB update operations using the `$inc` operator with a string value instead of a number.  The `$inc` operator is designed to increment a numeric field. Providing a string will result in the field being set to the string value instead of being incremented. This can be a hard-to-debug error in applications that rely on consistent numeric data.

## Bug Report
The bug occurs when using the `$inc` operator within an update operation on a MongoDB collection with a string value instead of a numeric value. The result will be an unexpected update.

## Solution
The solution is to ensure that the value being passed to `$inc` is a number. Correcting the code example demonstrates the correct usage, and prevents unexpected behaviours in the database operations.