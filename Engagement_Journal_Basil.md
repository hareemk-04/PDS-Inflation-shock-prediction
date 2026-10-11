Before I looked:
I predicted that official FRED data would have zero missing values and that all indicators would share the exact same monthly release schedule, and that oil price shocks would perfectly align with CPI spikes.

What I did, in order:
I downloaded the four raw CSVs, parsed the dates, and calculated the month over month target for Core CPI. My main dead end was attempting to merge the datasets directly because M2 velocity is quarterly the merge created massive blocks of NaN values that broke the monthly timeline.

What surprised me:
I found a missing Core CPI value for October 2025. I expected flawless government data, but manually checking the raw CSV and the FRED website confirmed the gap was real and not a code error.

What I revised:
I initially proposed predicting inflation a full quarter in advance to give portfolio managers maximum warning. However, once I saw that M2 Velocity is only reported quarterly, I realized that aligning it with a 3-month forward CPI prediction created unnecessary lagging complexity. Hence, we refined our proposal to a 1-month forecast horizon, which perfectly aligns with our baseline rule.

What I still don't trust:
I don't trust the interpolated CPI value for October 2025 as drawing a straight line might hide a genuine economic shock.
