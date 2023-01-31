# Central Bank of the Republic of Turkey's electronic data delivery system - EVDS

We can access the Central Bank of Turkey's Economic and Financial Data Delivery System (EVDS) using Python by obtaining an API key from the EVDS website. After registering on the website, users can access their unique key through the profile section. The EVDS also provides a user guide on their website, which can assist in downloading and utilizing the data. Here is the [Link](https://evds2.tcmb.gov.tr/help/videos/User_Guide_to_Access_EVDS_Data_by_Using_Python.pdf).

I have created a script that uses the EVDS API to download foreign assets data, convert it to USD, and then plot the data using the Seaborn and Matplotlib library in Python. The script can be easily modified by changing the series codes of the data, and I plan to update this repository with additional useful data and visualizations. Feel free to fork or copy the code for your own use.

## 1) sma4weeks() function / EVDS - Credit Card Payment Momentum: 

sma4weeks() function performs an analysis of the momentum of weekly credit card payments from Turkey using a single moving average (SMA). The purpose of this analysis is to understand the trend of the credit card payments over a specified time period and to determine if there is an upward or downward trend. The code starts by loading credit card payment data using the evdsAPI library, then formats the date column and calculates the weekly sum of credit card payments. The payments are then divided by 1 million to show them in millions. The payments are then plotted using a line plot and the 4-week rolling mean is calculated and plotted on top of the payments. The x-axis is labeled as "Date", the y-axis is labeled as "Weekly Credit Card Payments (billions of TRY)" and a title is added to the plot to describe the analysis. The x-axis dates are rotated 45 degrees to make them easier to read. The final plot is displayed and saved as a .png file.
In conclusion, the purpose of this analysis is to visualize the trend of credit card payments over time and to understand the momentum of these payments using a 4-week SMA.


![Logo](https://evds2.tcmb.gov.tr/themes/icons_new/logo.png)
