## Project Description
King County Real Estate is trying to predict home prices for its clients. This project aims to learn more about their county's home prices and the features that affect home prices. We build linear regression models to accurately predict the price of homes in their county. This would be useful to King County homeowners who are looking to sell their home to get an idea of their home's value before deciding to list it with a realtor.

**INTRODUCTION:** Insights Into The Housing Market Dynamics in Kings County, USA
## Overview
The housing market of Kings County, Northwest USA, is a dynamic market that has a lot of factors influencing house pricing. Understanding how and to what extent these factors impact pricing is really important for homeowners, real estate agencies, and other stakeholders.

This project aims to analyze housing sales data from King County, Northwest USA, employing multiple linear regression modelling. The objective is to derive meaningful insights for homeowners, real estate agencies, and other stakeholders about the factors influencing house prices, to make data-driven recommendations.

## Problem Statement
This project aims to conduct a thorough analysis of house sales data in King County, Northwest USA, utilizing multiple linear regression modeling techniques. The primary goal is to uncover insights into the factors influencing house prices in the region and offer data-driven recommendations for homeowners, real estate agencies, and other stakeholders. This advice is critical for homeowners to make informed decisions about investing in renovations that will maximize their return on investment when purchasing or selling a home.

Stake Holders
This project targets a diverse audience:

Homeowners: Individuals aiming to increase property value through informed decisions on renovations and enhancements.

Real Estate Agencies: Companies and agents seeking data-driven insights to facilitate effective home buying and selling for their clients.

**Objectives:**
To explore the Relationship Between the Square Footage of the Home and Housing Prices:
To investigate how the size of the house impacts the housing prices, and how significant is the correlation between living area size to price compared to the other independent variables.
To assess the Impact of Renovations on Housing Prices.
To analyze the impact of house upgrades on the sales price. How do renovated houses compare to non-renovated houses when other independent variables are constant?
Develop a Linear Regression Model to Predict Housing Prices:
To build and evaluate a linear regression model using the best features to predict house prices (price). Provide stakeholders with a predictive tool for estimating housing prices in Kings County.

## Business Understanding
This project addresses the core business challenges within the real estate market in King County, Northwest USA. Key stakeholders such as homeowners and real estate agencies are focused on gaining insights into the factors that impact house prices, enabling them to make informed, data-driven decisions in this dynamic market.

## Data Understanding
We used data sourced from King County Housing Dataset CSV. The data represents houses with information on price, bedrooms, bathrooms, sqft living, sqft lot, floors, view, and year built. The total data used was from 21597 homes split 80/20 for training and testing.

## OBSERVATION
A takeaway from this interpretation is that houses with an** AVERAGE quality of view might be under-valued since our understanding seems to indicate that it should be better than one with a FAIR view (+). More investigation of other features is needed to understand whether this can be explained by other variables, or if "AVERAGE" is actually undervalued.

1. Business Understanding
This project addresses the core business challenges within the real estate market in King County, Northwest USA. Key stakeholders such as homeowners, real estate agencies, and data science professionals are focused on gaining insights into the factors that impact house prices, enabling them to make informed, data-driven decisions in this dynamic market.

2. Data Understanding
We used data sourced from King County Housing Dataset CSV. The data represents houses with information on price, bedrooms, bathrooms, sqft living, sqft lot, floors, view, and year built. The total data used was from 21597 homes split 80/20 for training and testing. Variables include price, bedrooms, bathrooms, sqft living, sqft lot, floors, view, and year built.

Properties of variables of interest:
Price: Continuous numeric (float). Represents the sale price of houses in the dataset.
Bedrooms: Discrete numeric (integer). Represents the number of bedrooms in each house.
Bathrooms: Discrete numeric (integer).Represents the number of bathrooms in each house.
Sqft living: Continuous numeric (integer). Represents the total square footage of the living space in each house.
Floors: Discrete Discrete (integer). Represents the number of floors in each house.
View: Categorical (object). Represents the view rating of the property.
Year built: Discrete numeric (integer). Represents the year each house was built.

## Data Preparation.
  "### Exploratory Data Analysis"
  "#### Library Imports"
  "#### Load the Kings County Housing Dataset."
  "# Load the data into a dataframe and read the first five rows\n",
   "#### Column/Feature Description"
    "# Read the columns in the dataset\n",
    "#### Column Names and descriptions for Kings County Data Set\n",
     "# Gets the number of rows and columns in the KC dataset\n",
     "Gives a description of the numeric columns in the dataset."
     "# Numeric description of the columns\n",
      "Check the data type held by each column and the number of non-null values"
      "# Check the data type held by each column and number of non-null values\n",
      "Check the null values in each column"
       "Waterfront has 2376 null values, Year Renovated has 3842 and view column has 63 null values."
       "Address the null values in yr_renovated column."
       "78% (17011) of the houses in Kings County have not been renovated, I'll replace the null values with zero for this column."
       "# Replace the null values in the yr_renovated column with 0.00, which is the mode.\n",
        "Check the distribution of values in the waterfront and view columns."
        "Given that a significant percentage of the values in both columns is 0, the best replacement for the null values would be the mode."
        "# Replaces null values with the column mode\n",
         "# Check for null values\n",
         "There are no null values in the dataset."
         "##### Convert all non-numeric data values to numeric values for analysis."
         "The date column contains values of type string. Before any numerical analysis, this should be converted to a numerical data type"
         "# This converts the date column from string type to numerical type, which is the year the house was sold.\n",
          "# This checks for non-numeric values in the dataset and converts them to null values\n",
           "# Check the dataset for null values after conversion."
            "Since the data in the column is heavily skewed, it would be prudent to replace the null values with the mode."
            "For feature selection, we'll identify the independent variables that most affect our dependent variable, which is the price column, using a seaborn heatmap."
            "# Creates a seaborn heatmap that shows the correlation between the dependent variable(price) and the other independent variables\n",
            "**The most impactful features to the house price are square footage of the home(sqft_living), overall grade given to the housing unit, based on King County grading system(grade), square footage of the house apart from the basement(sqft_above) and The square footage of interior housing living space for the nearest 15 neighbors(sqft_living15)**"
            "#### FEATURE CLEANING FOR MODELLING"
            "##### Check for outliers in the feature columns"
            "# scale the columns for better visualization using boxplot\n",
            "All the columns have outliers. Since this will impact the model negatively, the cell below eliminates the outliers from the featured dataframe."
             "# Calculate IQR for feature columns\n",
             "# Define outlier boundaries\n",
              "# Find outliers\n",
               "# Drop indices of outliers\n",
                "# Visualize features without outliers\n",
                 "##### Check for duplicates"
                 "# Check for duplicated rowsb\n",
                  "There are two duplicate rows, these are deleted in the cell below."
                  "# Drop the two duplicates\n",
                   "Check feature colinearity using a correlation heatmap for better selection"
                    "## Data Analysis"
                    "#### Analysis 1: Explore the Relationship Between the Square Foot Living Area and Housing Prices:"
                    "# Creates a seaborn heatmap that shows the correlation between the dependent variable(price) and the other independent variables\n",
                    "**Observation:**\n",
    "\n",
    " In the heatmap above of the selected features against the dependent variable(`price`), square footage of the home(`sqft_living`) has the highest correlation to the house price (`0.54`). This indicates that square footage area of the home has a very high co-efficient to the price of the house.\n",
    "\n",
    " The regression plot above confirms this conclusion by showing that as the square footage of the home increases so does the price of the home across different grades of houses."
    "#### Analysis 2: Assess the impact of house renovations to the house price"
    "# Add a new column 'renovated' to show if a house is renovated or not.\n",
     "- A regression plot that shows the impact of house renovations on the dependent variable price, while controlling the other independent variables"
     "**Observation:**\n",
    "\n",
    "The Seaborn Implot shows a clear price increase in houses that have been rennovated in comparison to houses without rennovations. The Implot illustrates a linear regression model and also takes into account the other independent variables with a high correlation to price(`grade` and `square foot living space`)"
    "## Modelling\n",
    "***\n",
    "The following were the steps taken to come up with the model.\n",
    "\n",
    "### Steps taken while modelling \n",
    "1. Start with the data with outliers and create the baseline model.\n",
    "2. Add one predictor (independent) variable.\n",
    "3. Check the performance.\n",
    "4. Add a categorical variable.\n",
    "5. Repeat steps 2 - 4 until adequate performance is reached.\n",
    "6. Repeat these steps for the data without outliers and choose the best model.\n",
    "\n"
     "### I. First Iteration (Base model)"
     "highest correlation:  {'sqft_living': 0.7019173021377597}\n"
     "# find the correlation matrix of the data\n",
     "From the above result, **sqft_living** (which represents the square foot of living area) has the highest correlation with the price (0.7044283177851761), and is perfect for the baseline model, which is a simple linear regression.\n",
    "\n",
    "### Interpretation:\n",
    "\n",
    "### Simple Linear Regression Results\n",
    "\n",
    "Looking at the summary above, we can see that the regression line we found was\n",
    "\n",
    "* The model **is statistically significant** overall, with an F-statistic p-value well below 0.05\n",
    "* The model explains about 49.6% of the variance in price.\n",
    "    - indicating that approximately **49.6% of the variance in house prices is explained by the square footage of living space (\"sqft_living\").**\n",
    "* The model coefficients (`const` and `sqft_living`) are both statistically significant, with t-statistic p-values well below 0.05\n",
    "* If the sqft_living is $0ft^2$, we would expect price to be about $\\$-48,600$\n",
    "* For each increase of 1 square foot of living area, we see an associated increase in price of about $\\$283.4016$\n"
    "### Simple Linear Regression Visualization\n",
    "\n",
    "We'll also plot the actual vs. predicted values:"
    "### II. Second iteration\n",
    "\n",
    "### Adding Another Independent Variable\n",
    "\n",
    "Now, we expand from our simple linear regression to a multiple linear regression, in bid to improve the overall model performance. Let's try find the next highly correlated variable to price after sqft_living to use in our next iteration.\n",
    "\n",
    "But before that, we create a python **class** to avoid unnecessary repetitions of code so as to make the model iterations efficient and readable:\n"
    "# next highly correlated variable\n",
    "It looks like the number of `bathrooms` is the next most strongly _positively_ correlated predictor, so let's use that."
     "# check bathroom values before analysis\n",
     "Since the number of bathrooms should be discrete numerial value (i.e. we cannot have 2.75 bathrooms), we have to floor the values to a discrete value before any sort of analysis on the variable."
     "# reselect the variables\n",
      "# let's see the summary\n",
      "### Interpretation:\n",
    "\n",
    "### Second Iteration Regression Results\n",
    "\n",
    "Looking at the summary above, we can see that the regression line we found was\n",
    "\n",
    "* The model **is statistically significant** overall, with an **F-statistic p-value** well below 0.05\n",
    "* The model exhibits an **R-squared value of 49.7%**:\n",
    "    - indicating that approximately **49.7% of the variance in house prices is explained by the square footage of living space       (\"sqft_living\") and the number of bathrooms in the houses**\n",
    "    - slight improvement of 0.1%.\n",
    "* The model coefficients (`const`, `sqft_living` and `bathrooms`) are statistically significant, with t-statistic p-values well below 0.05\n",
    "* For each increase of 1 square foot of living area, we see an associated increase in price of about $\\$272.7382$\n",
    "    - this here is an decrease of $-10.66$ from the last model, which means that number of bathrooms was not meaningfully confounding in the relationship between sqft_living and price.\n",
    "* For each increase of 1 bathroom, we see an associated decrease in price of about $\\$19,120$\n",
    "\n",
    "* The model predicts a price of $\\$-59,890$ when `sqft_living` and number of `bathrooms` are 0. "
    "### Second Iteration Regression Visualization\n",
    "From the above model fit plot of the bathrooms variables appears a bit different from the sqft_living due to it's discrete nature."
    "#### ii.) Partial Regression Plot"
     "# plot partial regression plot\n",
     "This plot explains the unique contribution of each of the independent variables.\n",
    "\n",
     "This plot explains the unique contribution of each of the independent variables.\n",
    "\n",
    "- From left:\n",
    "    - the `sqft_living`  regression plot shows a linear relationship with a non-zero slope, and that means that it is beneficial to add *sqft_living* to the model, vs. having a model without *sqft_living* (i.e. a model with just an intercept and *bathrooms*)\n",
    "    - The partial regression plot for `bathrooms` is similarly showing the marginal contribution of `bathrooms` compared to a model with just *sqft_living*, albeit, a small one (seen by the near zero slope of regression line).\n",
    "\n",
    "A reasonable conclusion to reach, looking at these plots, is that both predictors are useful and should be included in the model (given the slight increase of the $R^2$ value), **BUT** the improvement is very little and this justifies the next model iteration."
     "### III. Third iteration\n",
    "### Adding all features\n",
    "\n",
    "Given the small improvement shown in the last iteration, we switch gears on this iteration and add all other independent variables and then check the performance. If the performance does not improve significantly or we see some redundancy, we choose a variable to drop and check the performance again. If the performance is positively impactly, we go to the next step."
     "# evaluate the correlations\n",
      "The number of floors should be discrete values so we floor the values to discrete values, before adding them to our model for analysis."
      "# we see the floors are floats, which doesn't make sense\n",
      "# we floor (ignore what comes after the decimal) the values \n",
      "### Interpretation:\n",
    "\n",
    "### Third Iteration Regression Results\n",
    "\n",
    "Looking at the summary above, we can see that the regression line we found was\n",
    "* The model **is statistically significant** overall, with an **F-statistic p-value** well below 0.05.\n",
    "* The model exhibits an **R-squared value of 56.1%** of the variance in price.\n",
    "    - Indicating that approximately **56.1% of the variance in house prices is explained by the model in this iteration and its predictor variables.**\n",
    "    - An overall improvement of 6.4% from the last model.\n",
    "* The model coefficients are statistically significant, with t-statistic p-values well below 0.05.\n",
    "* For each increase of 1 square foot of living area, we see an associated increase in price of about $311.33$.\n",
    "    - This increase from the previous model ($+38.89$) suggests that the number of bathrooms was confounding the relationship of the other variables.\n",
    "* For each increase of 1 bedroom, we see an associated decrease in price of about $-67,230$.\n",
    "* For each increase of 1 floor, we see an associated increase in price of about $55,900$.\n",
    "* For each increase of 1 square foot of the lot, we see an associated decrease in price of about $-0.3350$.\n",
    "* For each increase of 1 year, we see an associated decrease in price of about $-3,371.65$."
     " ### Model with All Features Visualization\n",
     " \n",
    " #### i) Plot fits"
     " #### ii) Partial regression plot\n",
    " \n",
    " We use a partial regression plot to display the contribution of each feature in the performance."
    "From the above partial regression plots we see that for some variables like `floors` and `sqft_lot` have slopes of near zero, meaning they do not contribute that much to the model.\n",
    "\n",
    "But we retain them because they keep the performance high while still having a low p-value, way below our $\\alpha$ of 0.05."
    "From here the model is at it's optimum state given all the predictors, now we add a categorical variable to it."
    "### Add a categorical variable\n",
    "We add atleast one categorical value from our dataset in the model. There are 4 categorical variables in our dataset, namely:\n",
     "Let's see their bar graphs below:"
     "# Lets see the bar graphs of the categorical features\n",
     "We choose a categorical predictor that will be interpretable in our model below. We go with `view`, as this categorizes the condition of the house from **NONE** to **EXCELLENT**. \n",
    "\n",
    "Since typically for categorical features the data type is a `string`, we have to encode it numerically to allow for regression modelling. \n",
    "\n",
    "So we create dummy variables (0's and 1's) representing True or False  (**One-Hot Encoding**):"
    "# select all needed features\n",
     "# create the dummy variables\n",
     "To avoid the **Dummy variable Trap** brought by when you can perfectly predict what one variable will be using some combination of the other variables, also known as **Multicollinearity**, we have to drop one of the dummy variables to break the collinearity.\n",
    "\n",
    "The dummy variable to drop is the `view_NONE`, since it is the lowest category of the views.\n",
    "\n",
    "This becomes our reference variable."
    "# drop the dummy variable view_NONE\n",
    "Now we check the impact of the categorical variable on our model:\n"
    "# Create new model with the categorical variable (view)\n",
    "### Final Iteration Regression Results:\n",
    "\n",
    "Looking at the summary above, we can see that the regression line we found was\n",
    ">This because a house only has one view quality so the model requires one view type to work correctly.\n",
    "\n",
    "#### Model Interpretation: \n",
    "\n",
    "* The model **is statistically significant** overall, with an **F-statistic p-value** well below 0.05\n",
    "* The model exhibits an **R-squared value of 59.5%** of the variance in price.\n",
    "    - indicating that approximately **59.5% of the variance in house prices is explained by the model in this iteration and its  predictor variables**\n",
    "    - An overall improvement of +3.4% from the last model.\n",
    "* The model coefficients are statistically significant, with t-statistic p-values well below 0.05\n",
    "\n",
    "* For each increase of 1 square foot of living area, we see an associated increase in price of about $\\$283.1530 $\n",
    "* For each increase of 1 bathroom, we see an associated increase in price of about $\\$+61,053.88$\n",
    "* For each increase of 1 bedroom, we see an associated decrease in price of about $\\$-57,029.00$\n",
    "* For each increase of 1 floor, we see an associated increase in price of about $\\$+58,199.17$\n",
    "* For each increase of 1 Square footage of the lot, we see an associated decrease in price of about $\\$-0.32359$\n",
    "* For each increase of 1 year built, we see an associated decrease in price of about $\\$-3020.64$\n",
    "\n",
    "\n",
    "* The intercept (const) implies that when all other variables are 0, and `view` is `NONE`, the price is  $\\$5,894,000$\n",
    "#### Interpretation of categorical variables:\n",
    "- Since our **`view_NONE`**is our reference category, we interpret the model summary in reference to it:\\\n",
    "i.e\n",
    "    - A shift from a house with **no view** to one with a **FAIR view** impacts the price positively by +$\\$126,599.94$   \n",
    "    - A shift from a house with **no view** to one with a **AVERAGE view** impacts the price positively by +$\\$84,639.98$\n",
    "    - A shift from a house with **no view** to one with a **GOOD view** impacts the price positively by +$\\$162,932.45$\n",
    "    - A shift from a house with **no view** to one with a **EXCELLENT view** impacts the price positively by +$\\$534,425.99$\n",
    "    \n",
    "### Observation:\n",
    "> A take-away from this interpretation is that houses with an** **AVERAGE** quality of **view** might be under-valued since our understanding seems to indicate that it should be better than one with **FAIR** view (+$\\$126,599.94$). More investigation of other features\n",
    "is needed to understand whether this can be explained by other variables, or if \"**AVERAGE**\" is actually undervalued."
     "### Objective 1: \n",
    "\n",
    "#### Explore the Relationship Between the Square Foot Living Area and Housing Prices\n",
    "\n",
    "**Conclusion:**\n",
    "- **Findings:** The analysis reveals a strong positive correlation (`r = 0.7`) between square foot living area(`sqft_living`) and housing prices(`price`). Larger properties tend to command higher prices in the Kings County housing market.\n",
    "- **Implications:** This high correlation suggests that the property size significantly influences housing prices, guiding decisions for real estate investors and homebuyers regarding property valuation and market positioning.\n",
    "\n",
    "### Objective 2:\n",
    "#### Assess the Impact of Rennovations on the Housing Price.\n",
    "\n",
    "**Conclusion:**\n",
    "- **Findings:** The Seaborn Implot shows a clear price increase in houses that have been rennovated in comparison to houses without rennovations. The Implot illustrates a linear regression model and also takes into account the other independent variables with a high correlation to price(`grade` and `square foot living space`) \n",
    "- **Implications:** Upgrading the overall grade and quality of your home, such as high-end finishes, better materials, and improved aesthetics, can lead to higher market prices. Focus on renovations that improve the grade of your home.\n",
    "\n",
    "### Objective 3:\n",
    "#### Develop a Linear Regression Model to Predict Housing Prices\n",
    "\n",
    "**Conclusion:**\n",
    "- **Findings:** The linear regression model, incorporating features `RM`, `LSTAT`, `PTRATIO`, and `INDUS`, achieves an R-squared (`R2`) score of `0.67` on the test set. This indicates that 67% of the variance in housing prices (`MEDV`) can be explained by these predictors.\n",
    "- **Implications:** Real estate agents and home owners can utilize this model for predicting housing prices based on property characteristics. It supports informed decision-making in real estate investments and pricing strategies."
     "## Recommendations\n"
     "1. **Focus on Key Upgrades:**\n",
    "   - Upgrading the overall grade and quality of your home, such as high-end finishes, better materials, and improved aesthetics, can lead to higher market prices. Focus on renovations that improve the grade of your home.\n",
    "\n",
    "2. **Enhance Living Space:**\n",
    "   - Increasing the living space (sqft_living) is a valuable investment. This could include adding extensions or converting unused areas (like basements or attics) into livable spaces.\n",
    "\n",
    "3. **Have knowledge of Kings County House Grading System :**\n",
    "   - Incorporate insights from Kings County on how they grade houses. The house grade has a high impact on the price, hence having knowledge of that grading system is important."
    
## Features selected
"X_all = ['sqft_living', 'bathrooms', 'bedrooms', 'floors', 'sqft_lot', 'yr_built', 'view'],

## Conclusion:
The final regression model achieved an R-squared value of approximately 59.5%, indicating that the selected predictor variables explain 59.5% of the variance in house prices. While the recommendations are data-driven and based on statistical analysis, individual factors and market conditions can vary, so it's essential to assess your property's specific situation before making any significant decisions.

# Recommendations:
The data analysis and regression modelling have provided valuable insights into the factors influencing house prices in the King County area. To maximize the estimated value of your homes, consider the following strategies:

Leverage Living Space: Increasing the square footage of the living area has a substantial positive impact on house prices. Consider renovation or expansion projects that can add more living space to your property. Each additional square foot of living area can potentially increase the estimated price by approximately $311.33*.

Bathroom Upgrades: Investing in bathroom upgrades can significantly boost your home's value. Each additional bathroom can increase the estimated price by approximately $61,053.88*. Consider modernizing and expanding your bathrooms to attract potential buyers.

Bedroom Considerations: While bedrooms are essential, be mindful of overinvesting in them. Each additional bedroom may decrease the estimated price by approximately $57,028*. Ensure that the number of bedrooms aligns with the needs of potential buyers.

Flooring and Layout: Houses with more floors tend to command higher prices. Consider optimizing your home's layout to make the most of the available space. Each additional floor can increase the estimated price by about $58,199*.

Lot Size Management: Pay attention to your property's lot size. Smaller lots may deter some buyers, and each square foot reduction in lot size can potentially decrease the estimated price by approximately $0.32*. Evaluate your landscaping and lot usage to make the most of your property.

Year Built: Keep up with yearly maintenance and consider renovations to modernize your home. Older homes tend to have lower estimated prices, with each year of age potentially decreasing the estimated price by around $3,020*.

View Quality Matters: If your property has a view, consider it a valuable asset. Homes with "excellent" views can command significantly higher prices, with each category upgrade potentially adding substantial value. Invest in maintaining or enhancing the quality of the view if possible.

Market Trends: Keep an eye on local real estate market trends. Factors like location, neighbourhood, and market demand can also influence house prices. Stay informed about the King County housing market to make informed decisions.

Consult a Real Estate Expert: To get a precise estimate of your home's value and tailor your strategy to your specific situation, consider consulting a local real estate expert or appraiser. They can provide personalized recommendations based on your property's unique characteristics.

## Contributors
**Patricia Ngugi**,
**Hanan Dayah**,
**JoakimTI**,
**Johnkul**.
