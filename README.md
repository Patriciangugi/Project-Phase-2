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
We used data sourced from King County Housing Dataset CSV. The data represents houses with information on price, bedrooms, bathrooms, sqft living, sqft lot, floors, view, aqnd year built. The total data used was from 21597 homes split 80/20 for training and testing. Variables include price, bedrooms, bathrooms, sqft living, sqft lot, floors, view, and year built.

Properties of variables of interest:
Price: Continuous numeric (float). Represents the sale price of houses in the dataset.
Bedrooms: Discrete numeric (integer). Represents the number of bedrooms in each house.
Bathrooms: Discrete numeric (integer).Represents the number of bathrooms in each house.
Sqft living: Continuous numeric (integer). Represents the total square footage of the living space in each house.
Floors: Discrete Discrete (integer). Represents the number of floors in each house.
View: Categorical (object). Represents the view rating of the property.
Year built: Discrete numeric (integer). Represents the year each house was built.

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

## Conclusion:
The final regression model achieved an R-squared value of approximately 59.5%, indicating that the selected predictor variables explain 59.5% of the variance in house prices. While the recommendations are data-driven and based on statistical analysis, individual factors and market conditions can vary, so it's essential to assess your property's specific situation before making any significant decisions.

## Contributors
**patricia Ngugi**,
**Hanan Dayah**,
**JoakimTI**,
**Johnkul**.
