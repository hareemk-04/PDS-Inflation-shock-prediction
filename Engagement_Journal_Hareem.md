Before I looked
I predicted that forecasting a full quarter ahead would be simple, that raw prices would be stationary and ready for modeling, and that Money Velocity would be our cleanest predictor.

What I did, in order
I took the raw files, standardized the date columns, and built the cleaning pipeline. My biggest dead end was when i started wroking for the M2 Velocity gaps; dropping missing rows deleted most of our dataset, so I had to implement a forward-fill instead. After I was done cleaning the data, I coded the EDA and transformed WTI and PPI into percentage changes to fix their upward trends.

What surprised me
I did notice a massive percentage spikes in the WTI oil data (January 1974 and May 2020) that I first thought were typos but then I cross checked them against the historical records and confirmed that they were real market events (the OPEC embargo and the post-COVID crash), not data errors.

What I revised
At first I thought predicting a quarter out would be the best approach for our stakeholders. However, when I was structuring the pandas merge, I noticed that applying quarterly M2 Velocity to a 3-month forward prediction was introducing unnecessary timeline gaps.

What I still don't trust
I am concerned that inflation patterns from the 1980s will perfectly match the 2020s, since the economy has naturally evolved over the last 40 years.
