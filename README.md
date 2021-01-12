# predict_energy_usage

Objective: 
 Analyze nationwide energy consumption data from July 2015 - December 2020 to try and forecast regional usage for a rolling 24 hour period

Business Understanding: 
 The economy is undergoing an energy revolution as we transition away from using fossil fuels as our primary energy source and towards cleaner, renewable options for generating electricity. In so doing, we are forced to confront the twin issues of storage and load management. 
 As it is currently designed, our electrical grid runs on a "Just in Time" net-zero model, meaning the goal is to generate the exact amount of electricity to meet demand at every hour of the day. Obviously, this is near impossible despite advances in technology and our best efforts. 
 While adjusting generating capacity while using fossil fuels is relatively simple and straightforward, more or less a matter of turning the generator up or down, the same is not true for renewable sources of energy. After all, the sun doesn't always shine and the wind doesn't always blow. This will require energy generated from those sources to be stored for later use paired with highly accurate forecasts of use to ensure that nobody is left in the dark.

Data Understanding:
 The data is sourced from the U.S. Energy Information Administration (https://www.eia.gov/realtime_grid/#/status?end=20210112T14)
 It has regional Demand and Generation numbers going back to mid-2015, though the sources of energy generation are not included in the data until the second half of 2018.

Data Preparation:
 Combine multiple files into a single Dataframe. Remove unnecessary columns and add others to account for formatting differences. Convert datatypes, mostly converting the Demand and Generation columns from strings to floats, though the 'UTC Time at End of Hour' obviously needed to be converted to Datetime.

Modeling:
 RNN using Time Series for Logistic Regression

Evaluation:

Deployment: