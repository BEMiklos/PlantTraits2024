Having carried out the measurements on the dataset, we can say that it is clean and does not require extensive preparation before starting the lessons. It contains 55k records, the training data and the target variables are all numbers, and null values are only in the auxiliary variables: the dataset also contains the distribution of the target variables, of which almost 30% are missing. We plan to use two different datasets, one in which we ignore this data and the other in which we add it.

On the target variables, it is worth using a log10 function, then converting to a standard distribution for each variable. Only the MODIS values have outliers, but this is natural given their power distribution property.

A weak correlation between the target variables is observed for most of them.

Some values of the climate (WORDCLIM) variables are strongly correlated (e.g. temp_seasonality and temp_annual_range). For better learning, it is worth considering not using them together. 

Soil values are mostly independent of each other, dimensional reduction should be considered. Adjacent depths are correlated, it is worth using them only at a certain resolution.

MODIS values by month are correlated with results from similar seasons. There is a strong correlation between the band values, it is worthwhile to select.

VOD values by m are correlated with adjacent values. Each decade is correlated with the other.
