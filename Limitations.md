Limitations:
The dataset is mostly highly reliable and it focused on the U.S. macroeconomic environment.
A minor limitation is that because it relies strictly on official, aggregated metrics (like CPI and PPI), it cannot measure underlying micro-level behaviors, like individual corporate pricing decisions or localized supply chain bottlenecks.However, this does not bring risk to our framed question, because bond managers trade based on the official macro numbers, not micro data. The only technical risk is accidental forecasting leakage—using M2 or PPI data representing a specific month before it was actually published. 

Our next step is to take action against the leakage, we will implement a  time-series cross validation split for our model training to ensure we only predict using historically available data.
