# Central Bank of the Republic of Turkey's electronic data delivery system - EVDS

 ![Logo](https://evds2.tcmb.gov.tr/themes/template01/images/Logo.png)
 
 ![Logo](https://evds2.tcmb.gov.tr/themes/icons_new/logo.png)



We can access the Central Bank of Turkey's Economic and Financial Data Delivery System (EVDS) using Python by obtaining an API key from the EVDS website. After registering on the website, users can access their unique key through the profile section. The EVDS also provides a user guide on their website, which can assist in downloading and utilizing the data. Here is the [Link](https://evds2.tcmb.gov.tr/help/videos/User_Guide_to_Access_EVDS_Data_by_Using_Python.pdf).

I have created a script that uses the EVDS API to download foreign assets data, convert it to USD, and then plot the data using the Seaborn and Matplotlib library in Python. The script can be easily modified by changing the series codes of the data, and I plan to update this repository with additional useful data and visualizations. Feel free to fork or copy the code for your own use.

## 1) sma13weeks() function / EVDS - Credit Card Payment Momentum: 

The purpose of this function is to plot the yearly change rate of personal credit card loan size along with its 13-week simple moving average (SMA).

The code uses the EVDS library to fetch the data for the credit card size YoY change, which is the difference between the current year's credit card loan size and the previous year's credit card loan size expressed as a percentage. The data is loaded for a specified time range between a start date and an end date.

The code then calculates the 13-week SMA for the credit card size YoY change data. The SMA is calculated by taking the average of the current and previous 12 weeks' data points, effectively smoothing out short-term fluctuations in the data and providing a clearer picture of the underlying trend.

Finally, the code plots both the credit card size YoY change and its 13-week SMA using a line plot. This allows the user to visualize the trend in credit card loan size growth and assess whether there is a momentum trend or not. The YoY change rate plot provides insight into how credit card loan size has changed over time, while the 13-week SMA plot provides a clearer picture of the underlying trend in the YoY change rate data.

## 2) MonthlyReturnHeatMap() function / EVDS - USD/TRY and BIST100 Monthly Return Visualization:

This function is to create a heatmap of the monthly returns of the USD/TRY and Istanbul Stock Exchange between January 1, 2018 and January 30, 2023. The code accesses the exchange rate data through the evdsAPI, a Python library for accessing data from the CBRT – Central Bank of the Republic of  Türkiye (EVDS) database.

The code first loads the data using the evds.get_data() method, and formats the date column using the pandas library. The code then extracts year and month information from the date index and divides the var1_1 column by 100 to convert the data into a percentage.

The code then creates a pivot table from the data using the pandas pivot method, and creates the heatmap using the seaborn library. The heatmap uses the cmap parameter to specify the color map (RdYlGn) and the fmt parameter to specify the format of the annotations in the heatmap. The vmin and vmax parameters are used to set the minimum and maximum values for the color scale, respectively.

This code can be useful for visualizing the monthly returns of the usd/try, xu100 or however you want from EVDS  how they change over time, providing insights into trends and patterns in the data. I make the code dynamic so you just need to change parameters if you want to see other financial instrument’s monthly returns. 


## 3) RegressionAnalysis() function / EVDS - TL Credit and Import Size YoY Change Relationship:

This code is a script for performing regression analysis between two variables in order to determine the relationship between them. The RegressionAnalysis function is the main function of the script that performs the regression analysis between two variables. The function takes in several parameters, including the names of the two variables, their corresponding names, the start and end dates for the data, and the names of the columns in the data frame that correspond to the two variables.

The function first loads the data using the evds.get_data() method and formats the date column. It then drops any NA or ND values and converts the data type of the second variable to float. The data is then saved as an Excel file for future reference.

The function then calculates the correlation between the two variables and performs an ordinary least squares (OLS) regression using statsmodels. The regression results are printed in the form of a summary. The script also plots the two variables over time and a scatter plot with a regression line. The plots are generated using matplotlib and seaborn.

Finally, the script sets the parameters for the two variables and calls the RegressionAnalysis function to perform the analysis.


## 4) interestrates() function / EVDS - Credit and Deposit Interest Rates:

The purpose of the interestrates() function is to plot a line graph of the interest rates over time for the given variables in the vars_dict dictionary.

The function first loads the data using evds.get_data() function, which retrieves the historical data for the given variables in the dictionary, with the specified start and end dates. The date column is formatted using pd.to_datetime(), and the dots in the column names are replaced with underscores to avoid any errors in plotting.

Next, a color palette is set for the line plots, and a line plot is created for each variable using sns.lineplot(), with the x-axis as the date column and the y-axis as the variable code in the dictionary. The last value of each line is annotated using plt.text(), which displays the value at the end of each line.

Finally, the graph title, x-label, y-label, and legend are added using plt.title(), plt.xlabel(), plt.ylabel(), and plt.legend(), respectively, and the plot is displayed using plt.show(). Metadata [Link](https://www.tcmb.gov.tr/wps/wcm/connect/933493cb-5251-43f3-af70-920eee213041/RIPMetaveri-1_Haftal%C4%B1k_Mevduat_Ag%C4%B1rl%C4%B1kl%C4%B1_Ortalama_Faiz.pdf?MOD=AJPERES)


