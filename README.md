# Dallas County Animal Shelter Intake and Outcome Analysis (2023-2025)

This is the final milestone project for CHIP 690.335. 
For this project, I utilized Python to answer research questions related to animal intake and outcome groups from the Dallas County Animal Shelter. The deliverable was a Jupyter Notebook that demonstrates data retrieval and cleaning, data analysis, and data visualization.

## Research Questions

1. Do specific intake types correlate with different outcome type likelihoods for cats and dogs at the Dallas County Animal Shelter from 2023-2025?

2. Does the intake type correlate with the expected lenght of stay?

3. Is there a significant, consistent seasonal trend in the number of intakes at the Dallas County Animal Shelter?

## Data Source

The data for this project was obtained from a single source: [Dallas County Animal Shelter Data](https://www.dallasopendata.com/Services/Dallas-Animal-Shelter-Data-Fiscal-Year-2023-2026/uyte-zi7f)

## Data Cleaning and Prep

The dataset was cleaned by removing rows with missing critical data. The data was filtered to meet the needs of this analysis:

- Animal type was filtered for only cats and dogs.
- Intake condition was filtered to exclude animals that were deceased on arrival
- Intake type was filtered to exclude animals not being housed at the shelter
- Length of stay was calculated 
- A live release category was defined to include only the following outcome types: Adoption, Returned to Owner, Foster, Transfer, TNR
- A new outcome group column was created to differentiate between animals with an outcome type of live release, animals that were euthanized or died, and other/unknown
- Animals with an other/unknown outcome were filtered out

## Data Analysis & Visualizations

The analysis was conducted using a Jupyter Notebook. The dependencies needed to run the notebook can be found in the requirements.txt file. 

The generated visualizations include:

1. A pie chart of the overall percentage of cats and dogs with a live release outcome vs. a deceased outcome
2. A bar graph of animal types vs. outcome group (counts)
3. A stacked bar chart of intake condition vs. outcome group (percentages)
4. A boxen plot of length of stay (in days) by intake type. A boxen plot was used to handle outliers.
5. A line graph of monthly intake over time to display seasonal trends in animal intakes.

## Summary of Key Insights
- **Mostly Postive Outcome**: The pie chart shows that the overall percentage of animals with a live release outcome is significantly greater than those in the deceased group. However, the percentage is still lower than what is needed for no-kill status.
- **Better Chance for Dogs**: The bar chart shows that a greater percentage of dogs than cats had a live release outcome. This indicates the shelter should focus on improving outcomes for cats.
- **Intake Condition Significantly Affects Outcome**: The stacked bar chart shows significant correlation betwen intake condition and outcome. Notably, animals that appeared within normal limits on intake were much more likely to have a live release outcome than those that appeared sick or injured. Interestingly, those described as geriatric were significantly less likely to have a live release outcome than those that appeared sick, injured, or underage. This indicates that geriatric animals are at increased risk when entering the shelter and extra care and/or effort should be made to improve their outcome.
- **Length of Stay**: There was some variation between intake type and length of stay, with certain types, like TNR, having an expectedly lower length of stay than other types of intake.
- **Seasonal Trends**: The line graph revealed expected season trends during the summer months (notoriously known as "kitten season"). There were unexpected decreases in intakes at times that corresponded to news posts about the shelter temporarily closing intakes due to disease or full kennels. 
