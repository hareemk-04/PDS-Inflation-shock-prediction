Prompt 1: 
We asked the AI to explain the concept of aligning quarterly time-series data (M2 Velocity) with monthly data (CPI) without causing forecasting leakage. 
Takeaway: We took the conceptual suggestion to use a "forward-fill" method. I read the pandas documentation for ffill() myself and manually verified the output dataframe to ensure Q1 data only populated January, February, and March.

Prompt 2: 
We asked the AI to help understand a ValueError: Missing column provided to 'parse_dates' error when loading the CPI CSV. 
Takeaway: The AI correctly explained that the column name in the code didn't match the file. I rejected the AI's first suggestion to open the CSV in Excel and rename the column by hand and instead wrote pandas code to rename the column safely.

Prompt 3: 
We asked the AI for the matplotlib syntax to plot a "twin axis" chart so we could overlay the raw WTI oil price and its percentage change on the same graph.
Takeaway: We took the twinx() function syntax. I checked the code line by line to ensure I understood it, and I adjusted the plotting colors, labels, and titles myself.
