# Uncommon Python Bug: Silent Failure with Non-Numeric Data in Average Calculation

This repository demonstrates a subtle bug in a Python function designed to calculate the average of a list of numbers. The function correctly handles empty lists, but it silently fails when the input list contains non-numeric data.

## Bug Description

The `calculate_average` function calculates the average of numbers in a list. It handles empty lists gracefully. However, if the input list contains elements that are not numbers (e.g., strings), it will raise a `TypeError` exception, which is not explicitly handled in the function.

## Bug Solution

The solution involves adding error handling to check for non-numeric data types before performing the calculation.  A `try-except` block effectively catches and handles potential `TypeError` exceptions, providing a more robust way to prevent unexpected errors and maintain program stability.