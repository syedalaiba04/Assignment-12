1. Court Verdicts
Verdict 1: Remove duplicate rows — KEEP

The dataset had one exact duplicate row. Removing it was reasonable because it was an identical copy of an existing record.

Verdict 2: Convert prices into numbers — KEEP, WITH MODIFICATION

The price column contained values stored as text. One value, 1,250, could not be converted directly because of the comma. Removing the comma before converting the column solved this formatting issue.

Verdict 3: Fill missing prices — REJECT

There was one missing price. I decided not to fill it with an estimated value because there was no evidence of what the actual price should be.

Verdict 4: Remove unusually high prices — REJECT

A high price does not automatically mean that the data is incorrect. The value 1,250 was kept because deleting it without further evidence could remove a valid observation.

Verdict 5: Standardise item names — MODIFY

Changing all item names automatically could hide differences in the original data. I decided to inspect the labels first and preserve the original names instead of changing them without confirmation.

Verdict 6: Convert dates into datetime format — KEEP

This was useful because it allows dates to be sorted and analysed properly.

Verdict 7: Keep the original dataset unchanged — KEEP

I worked on a separate copy so that the original data would remain available for comparison.
2. Log Rows
- Initial inspection: Loaded the original dataset and found 97 rows and 6 columns.
- Missing values: Found one missing value in the price column.
- Duplicate check: Found one exact duplicate row.
- Price conversion: Direct conversion failed on the value 1,250 because it contained a comma.
- Duplicate removal: Removed the exact duplicate from the working copy, leaving 96 rows.
- Price cleaning: Removed commas before converting the price column into numeric values. The missing price remained missing.
- Date conversion: Converted the date column into datetime format.
- Final check: The cleaned dataset contained 96 rows, with 95 non-missing prices.
3. Reflection
This task helped me understand that cleaning data is not just about removing everything that looks unusual. Some values might look incorrect but could still be valid.

Using AI was helpful because it suggested different ways to inspect and clean the dataset. However, I realised that I should not accept every suggestion without checking it. For example, automatically deleting high prices or filling missing values could change the actual meaning of the data.

I also noticed that even simple code can produce errors. The class notebook showed a KeyError when an attempt was made to select columns from the result of duplicated(). This reminded me that code needs to be tested rather than blindly copied.

Overall, I learned that AI can help with data cleaning, but the final decisions should be based on the actual dataset and evidence. It is important to preserve the original data and make only changes that can be justified.
