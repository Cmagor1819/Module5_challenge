# Module5_challenge
Challenge Instructions:

This challenge displays the results and relationships between squamous cell carinoma and the treatments that the mice recieved.
In this study, 249 mice that were identified with SCC recieved treatment with range of regimens.
Over 45 days tumor size and SCC treatments were observed and recorded.
This study also displays the performance of Capomulin, Pymaceuticalss drug of interest, compared to others.

Challenge Steps:

1.Prep the data
2.Summary Statistics
3.Create bar and pie charts
4.Calculate quartiles, outliers, and generate box plot
5.Generate line and scatter plots
6.Calculate correlation and regression
7.Write analysis
Summary Stats:

This section creates a dataframe of summary stats.

Bar and Pie Charts:

This section generates two bar charts using the Pandas method and the pyplot method
The pie charts are generated showing distribution between male and female mice using pandas and pyplot methods

Quartiles, Outliers, and Box Plot:

This section calculates and shows the final tumor volume across each regimen.
We also show the calculations for quartiles and IQR, and determine if any outliers exist.

Line Plot and Scatter Plot:

This section shows a select mouse that was treated and generates a line plot.
This also generates a scatter plot of the same stats.

Correlation and Regression:

This section calculates and shows the correlation between mouse weight and average tumor volume.
Also plotting the linear regression model on top of scatter plot.

Analysis:

This section at the top of the code describes the conclusions that were drawn from the data and summaries.

I got/regerenced the following code from Xpert Learning Assistant/GitHub
duplicate_mice = merged_df.loc[merged_df.duplicated(subset=["Mouse ID", "Timepoint",]), "Mouse ID"].unique()
clean_mouse_df = merged_df[merged_df["Mouse ID"].isin(duplicate_mice) ==False]
def outliers(regimen):
    regimen_data = merged_timepoint_df.loc[merged_timepoint_df["Drug Regimen"] == regimen]["Tumor Volume (mm3)"]
capo_df = merged_df.loc[merged_df["Drug Regimen"] == "Capomulin"].groupby("Mouse ID")
for treatment in range(len(merged_timepoint_df)-1):
unique_mice = clean_mouse_df[["Mouse ID", "Sex"]].drop_duplicates()
