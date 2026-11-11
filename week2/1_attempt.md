1. Diagnosis
The original file teaching_prices_messy.csv contains 97 rows and 6 columns. The dataset represents illustrative weekly prices across two cities and four product categories.

The following data-quality issues were identified during the initial inspection:

1. Duplicate Observation

The observation for Staple A in City 1, dated 8 January 2026, with a recorded price of 99.5, appears twice.

2. Missing Value

The observation for Pulse C in City 2, dated 1 January 2026, has a missing price value.

3. Extreme Price

Sweetener D in City 1, dated 22 January 2026, has a recorded price of 9999, which is significantly higher than its other recorded prices.

4. Inconsistent Price Formatting

Staple A in City 2, dated 15 January 2026, has a price recorded as 1,250, unlike the standard numeric formatting used elsewhere.

5. Inconsistent Product Label

The label oil b appears on 5 February 2026 in City 1 instead of the consistently used Oil B. Its recorded price is 108.5.

6. Inconsistent Data Type

The price column is interpreted as text rather than a consistent numeric data type due to mixed formatting and missing values.

2. Planned Decisions
1. Duplicate Observation

Remove one copy after verifying that both records are identical.

2. Missing Value

Retain the observation and flag the missing price. Do not replace it with an estimated value.

3. Extreme Price (9999)

Retain the original value and flag it for further investigation. Do not automatically delete or replace it.

4. Inconsistent Price Formatting (1,250)

Standardize the numeric formatting if appropriate and flag the unusually high value for investigation.

5. Inconsistent Product Label (oil b)

Retain the original label and investigate the observation before making any corrections.

6. Inconsistent Data Type

Convert valid dates and prices into their appropriate data types while preserving missing and suspicious values.
