# Data Profiling Report

## Issues Found
1. **Duplicate Row:** ORD0016 appears twice.
2. **Missing Values:** ORD0008 is missing a City. ORD0038 is missing Quantity.
3. **Text Inconsistencies:** ORD0023 has `" laptop "` (extra spaces). ORD0069 has `"online"` (lowercase).
4. **Date Inconsistencies:** ORD0090 is formatted as `2026/04/15` instead of `YYYY-MM-DD`.
5. **Logical Errors:** ORD0052 has a Discount of 120% (Impossible).
6. **Calculation Error:** ORD0063 Revenue doesn't match the math.

## How I will handle them (Cleaning Plan)
1. Remove duplicates based on Order_ID.
2. Impute missing City (assign "Unknown").
3. Trim whitespace and standardize capitalization on Product and Sales_Channel.
4. Fix the date format to standard Date type.
5. Cap the 120% discount at 100%.
6. Recalculate Revenue in Power Query to ensure accuracy.
