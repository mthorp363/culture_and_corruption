# Hofstede's 6 Dimensions and Corruption

Split project two parts, this project looks at the correlation between Hofstede's 6 dimensions of culture (used in cultural relativity for comparing cultures) and corruption to see if the dimensions are connected to culture. Following this, linear regression and the coefficient of determination are explained. Finally, a linear regression model is used to asses how missing values in the dataset are best handled.

## [Executive Summary (part 1)](https://github.com/mthorp363/culture_and_corruption/blob/master/Main.ipynb)

For companies working internationally, it is important to be aware of the corruption they may need to deal with in new countries. However, data is not always available to make a meaningful comparison and therefore, Hofstede's 6 dimensions will be compared with a variety of different corruption ratings to see if any correlate. Later, this can be used to develop a predictor.

Key insights:

- There are two pairs of Hofstede values with strong negative correlation (long term orientation and indulgence and individualism and power distance).
- The corruption ratings strongly correlate aside fom the Bertelsmann index.
- "Power distance" correlated the highest with 4 of the corruption rankings.
- "Masculinity" showed the least correlation with the corruption rankings.
- The "CPI Score 2019" was the most useful corruption ranking (best indicator of the correlation trend).
- "Bertelsmann" was the least useful corruption ranking.

![Hofstede's 6 Dimensions and CPI correlation](corruption_features.png "Hofstede's 6 Dimensions and CPI correlation")

Data from [Transparency International's CPI](https://www.transparency.org/en/cpi/2019/results/table) and [Hofstede's 6 dimensions of culture](https://geerthofstede.com/research-and-vsm/dimension-data-matrix/).

## [Executive Summary (part 2)](https://github.com/mthorp363/culture_and_corruption/blob/master/Part%202.ipynb)


In Part 1 of culture and corruption, the cultural dimension which showed the most correlation with corruption levels was power distance. In Part 2, a linear regression model is built from scratch to show how the model works and then SkLearn's linear regression model is used to show how different methods for handling missing values can have a strong impact on the effectiveness of the model. A boxplot of the coefficient of determination from 500 iterations of linear regression for each method is created. Insights are as follows:

- Using the column mean has the worst performance overall.
- Using linear interpolation, outliers or dropping missing values had the same mean value.
- Dropping the values altogether had the highest potential value.
