1.
We noticed that there is a missing CPI value in October 2025. We decided to use linear interpolation to fill the gap. We did not go for dropping the row entirely because time-series forecasting requires continuous dates.

2.
We then observed that the M2 Velocity is a quarterly metric, which caused NaNs when joined to monthly data so we decided to use a forward fill so the quarterly values carry into intermediate months without leaking future data we rejected dropping the NaNs, which would have lead to the deletion of two thirds of our dataset.

3.
We noticed extreme WTI oil price spikes in 1974 and 2020 and decided not to change them as these represent actual historical energy shocks which are highly relevant for predicting inflation.

4. 
We saw that the first row (Sep 1986) had NaNs after calculating percentage changes so we dropped the first row we did not choose to fill it with zero, because that would mean 0% inflation.

5.
Variables are on completely different numerical scales like prices vs indices so we decided not to change them during cleaning as standardization belongs in the machine learning phase and not in the raw data cleaning phase.

The data dictionary is as follows:
observation_date: datetime, first day of the month, FRED
Core_CPI: float, Index, Core CPI less food & energy, FRED
CPI_pct_change: float, Percentage, MoM Core CPI growth, Calculated
WTISPLC: float, USD/Barrel, WTI Crude Oil Price, FRED
PPIACO: float, Index, Producer Price Index, FRED
M2V: float, Ratio, M2 Money Velocity, FRED (forward-filled)
