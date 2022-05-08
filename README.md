# stocks_performance_proj
US stocks dataset with financial indicators was analyzed to determine performance trends.

<b>Background</b>

I worked with a dataset found on Kaggle that consisted of more than 200 financial indicators, that are commonly found in the 10-K filings that publicly traded companies release every year. The data is for US stocks from year 2014 to 2018.
Financial indicators such as current ratio, debt-to-equity ratio, asset turnover, net profit margin, etc. were analyzed in the EDA. Performance was compared across different sectors and price variation over four years was analyzed to determine sectors for stocks that would have been a good buy.

The data also contains sector that each company belongs and class of each stock or its price variation the following year. The class would indicate whether a trader should buy a stock at beginning of the year and sell at year-end for profit or if the trader should not buy the stock since there will likely be loss of capital. For instance, if a price variation for a stock is positive in 2015, the stock will have a class of 1 in the year 2014.

<b>Dataset at a glance </b>

The dashboard shown below summarizes some of the key attributes of the data. There were 4,980 distinct US stocks provided from 2014 to 2018 with a median price variation of 3.6%. Median was used as a measure of central tendency since a lot of the features in the dataset including the price variation target had a number of outliers.

![](/images/overall_dashboard.JPG)

Current ratio was used as a measure of liquidity, debt-to-equity ratio for solvency, asset turnover to measure efficiency, and the net profit margin to assess the profitability of each company. The performance across all these 4 measures has gotten worse since 2014, since current ratio, asset turnover, and net profit margin were all relatively high and debt to equity ratio was low in the beginning. 

Overall, a current ratio of 1.76 indicates that most of the companies have enough cash to meet their liabilities while using their capital effectively. The debt to equity ratio also looks good overall and shows strong financial leverage. Asset turnover ratio of 0.48 seems to be on the lower side, but it could be since some sectors such as utilities tend to have a lower asset turnover relative to others. The net profit margin, however, seems to be pretty low – to assess across the best and the worst performing sectors I applied a filter for the sector.


<b>Financial Services Sector Performance</b>

Majority of the stocks in the dataset are from the financial services sector and overall in terms of class 1 stocks and price variation this was one of the best performing sectors over the five years.

![](/images/financial_services_sector_dashboard.JPG)

Though the current ratio and asset turnover seem to be very low, a relatively strong net profit margin of around 20% could be contributing to the higher percent variation relative to the other sectors. 2018 was a great year for this sector, with the net profit margin rising significantly after a slight drop in 2017 and debt to equity ratio also getting on the lower side.

<b>Energy Sector Performance</b>
The energy sector was one of the worst performing sectors in terms of the median percent price variation over the five years. While the current ratio and asset turnover look much better when compared to the financial services sector, the median net profit margin is a lot smaller. In the years 2015 and 2016 the net profit margin dropped close to -5% but showed some recovery since 2017. But the current ratio has been declining since the year 2016.

![](/images/energy_sector_dashboard.JPG)

<b>How has price variation changed for all sectors over last few years?</b>

Here I decided to look at the trend for price variation and class 1 stocks over the five years.

![](/images/price_variation_class_by_year.JPG)

In the year 2018, steepest drop seemed to have happened for Basic Materials, and Real Estate sectors. This makes sense since 2018 was one of the worst years in a decade for some sectors. As an example, home sales in Manhattan fell 14 percent in 2018, and this was industry’s steepest drop since 2009 mainly due to an oversupply of high-end apartments and demand from foreign buyers cooling down.
And Basic materials sector also had a crash in 2018 due to the US-China trade war, concerns over lower demand from China and raw material costs increasing.
Utilities sector was relatively one of the best performers during the market decline in 2018 which makes sense since it is known to be a defensive sector. Investors tend to put money into utility stocks to escape market volatility. The pandemic in 2020 however showed a slightly different trend since the utility sector was also adversely impacted by the crash. 
There was a recovery in 2019, which led to a rise in the fraction of stocks that should be purchased to rise in 2018 for all the sectors. 

<b>Data Quality Issues</b>

During the analysis I found that there were some issues such as missing values and outliers in the features and target in the dataset. Some of the issues are summarized in the dashboard below.

![](/images/missing_values.JPG)

Financial Services sector had the greatest fraction of missing values – I analyzed the missing values for 3 important financial indicators here Price to Earnings ratio that had around 31% missing values, Earnings per Share around 20% missing values, and Return on Equity also had 31% missing values.
Across the 6 key financial indicators, the financial services sector had around 40% missing values which was the highest relative to all other sectors.
Types of financial services companies with missing values include insurance, asset management, and brokerage firms. 

Another issue with the data is the large number of outliers. Some sectors such as Real Estate, Technology, Financial Services, and Communication Services had majority of the outliers.

![](/images/outliers_in_dataset.JPG)

The outliers are present for some important financial indicators such as P/E ratio and the percent Price Variation target also seems to be impacted for years before 2016 for many sectors. 


<b>Average Financial Indicators by Sector Comparison</b>

I compared P/E ratio across all the sectors and found that the top 3 performers were Real Estate, Financial Services, and Consumer Defensive sectors. 
Debt to Equity ratio seems to be relatively low for Technology, Consumer Cyclical and Consumer Defensive sectors. 

![](/images/pe_ratio_de_ratio_by_sector.JPG)

Here as well, median was used due to several outliers in the data.
When I looked at the combination of these financial indicators, Consumer Defensive was one of the best performing sectors over the 5 years since it had a price to earnings ratio of around 19 and its Debt-to-Equity ratio of 0.44 was also relatively on the lower side. 


<b>Number of Best and Worst Performing Stocks by Sector</b>

Here I analyzed the number of stocks for each sector with a class of 0 or 1 for 5 consecutive years.
Energy and healthcare sectors were the worst performing since healthcare had 88 companies that had a class of 0 for 5 consecutive years which was the highest across all sectors. While energy did not have any stocks with class of 1 for all five consecutive years. 

![](/images/best_worst_performing_stocks_by_sector.JPG)

Financial services sector had the highest number of class 1 stocks for all years, while utilities had the greatest fraction of class 1 to class 0 stocks.
Based on this analysis I picked two companies – Amazon and GoPro within the Technology sector and looked at their performance in more detail.


<b>Analyzing two best and worst performing stocks</b>

Below is an overall comparison between two companies – Amazon that had a class of 1 for five consecutive years and Go Pro that had a class of 0 for five consecutive years.

![](/images/amzn_vs_gpro_1.JPG)

Amazon’s gross margin of 40.3% was higher in 2018 relative to 31.5% for GoPro.
Also, their revenue growth year over year was of 30.9% compared to a decline by 2.7% for GoPro.
And Amazon’s stock price growth has been a lot more consistent compared to GoPro. And ever since the pandemic, they have had a really strong momentum as their operating income nearly doubled to $6.2 billion by the end of 2020.
For GoPro on the other hand, stock price looks a lot more volatile over the last five years – even though now as they are growing their direct to consumer business, they are seeing improved gross profit margins.

The charts below show operating and free cash flow to compare performance in terms of the liquidity between Amazon and GoPro. 

![](/images/amzn_vs_gpro_2.JPG)

Operating cash flow is the positive cash flow that a company can use to run its business and grow its operations. Free cash flow is often a good indicator of cash that a company generates from its normal operations before interest payments and after subtracting any money spent on capital expenditures. GoPro's free cash flow remained negative since the year 2016. This may have limited GoPro’s ability to grow their operations by investing in new products or expanding via acquisitions. Amazon, in contrast has shown strong growth in their operating and free cash flows. In 5 years from 2014, Amazon’s free cash flow grew around 10 times to 19.4B in 2018.


Lastly, I compared the return on tangible assets and asset turnover for Amazon and GoPro.These metrics can help investors understand how effectively companies are using their assets to generate sales.

![](/images/amzn_vs_gpro_3.JPG)

Amazon's asset turnover decreased in each of the last five fiscal years from 2016. And even after 2018, the asset turnover continued to decline and Amazon hit its five-year low in December 2020 of 1.4. While GOPRO in contrast had a significant increase in 2018 as the asset turnover rose to 1.64 but they continued to have a negative return on tangible assets. 

Besides asset turnover, across all the other financial indicators Amazon clearly has been a better performer than GoPro from 2014 to 2018 and therefore had a class of 1 for five consecutive years. 
