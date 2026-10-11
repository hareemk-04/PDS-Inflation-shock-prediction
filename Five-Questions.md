1. What is a row?
A single row in our dataset represents a single month of aggregated US macroeconomic activity. We checked the observation_date column and we are confident it steps by exactly one month per row.

2. What is the unit of the outcome?
It is a percentage. We transformed the raw CPI index using a math formula to get month-over-month percentage growth and we are highly confident that it is in line with our work.

3. What is the timeframe?
The data covers exactly 40 years, from September 1986 to August 2026. We are highly confident for this because we confirmed this by the min and max dates in our code.
5. Who is missing?
The data misses undocumented shadow economy transactions. Also, the raw data was missing the October 2025 CPI value which we had to interpolate and thus we are sure to have a more workable data now.

6. What was the sampling frame?
The frame is based on official administrative and survey models produced by the BLS and Federal Reserve. Our confidence for this is medium, because the exact survey mechanics aren't detailed in the FRED export.
