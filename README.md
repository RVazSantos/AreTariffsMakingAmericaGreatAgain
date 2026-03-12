# Are Tariffs Making America Great Again?

![Data Analytics](https://img.shields.io/badge/Data%20Analytics-Project-blue)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-150458?logo=pandas&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-Visualization-E97627?logo=tableau&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Modeling-blueviolet?logo=scikitlearn&logoColor=white)

An in-depth analysis of the tariff policies introduced in 2025, exploring their policy
background and assessing their economic impact to date.

<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/Cover.png" alt="Alt text" width="800"/>

## Business Case

The U.S. Department of Commerce requested a review of the 2025 tariff policies, including their scope and their economic effects to date.  
This analysis aims to support policy reassessment and inform potential future actions.

## Objectives

### 1. Scope Evaluation

- Verify whether the United States has a negative trade balance.
- Assess whether the main targeted countries and product categories are the most relevant.
- Identify the sectors most affected by tariff policies.

### 2. Policy Effect Assessment

- Evaluate changes in the trade balance.
- Analyze the impact on the main importing countries.
- Evaluate changes in imports of targeted products.
- Examine domestic production and unemployment trends.
- Evaluate the Consumer Price Index (CPI) trend and generate forecasts up to 2027.

## Deliverables

- Timeline of major 2025 tariff policy implementations.
- Interactive dashboards covering background, effects, and forecasts.
- Overall evaluation using a custom assessment framework.
- Policy recommendations for potential future actions.

# Dashboards

## Background Context: Country View
<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/background_country.png" alt="Alt text" width="800"/>

**Key takeaways:**

- Negative Commercial Balance overall and
with most countries;
- Import and Export values are stable
between 2022 and 2024;
- Main Import partners are also main
Export partners;

## Background Context: Product View

![Dashboard Demo](https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Videos/Overview_Product_gif.gif)

**Key takeaways:**
- "Machinery and Electrical Equipment" is
the main Product Section;
- Main Chapters are "Motor Cars" and
"Petroleum Oils";
- Top 4 partners (EU, CN, MX, CA) account
for more than half of all imports;

## Tariff Timeline

![Dashboard Demo](https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Videos/Timeline_gif.gif)

**Key takeaways:**

- Main countries targeted: Canada, Mexico and China;
- Main products targeted: Aluminum, Steel, Automobiles,
Auto parts, Copper and Timber;

**Out of Evaluation Scope:**
- Copper, Timber and Trucks (happened too late to measure effects)

## Impacts: Product View

![Dashboard Demo](https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Videos/Impact_Products_gif.gif)

**Key takeaways:**
- Affected sections of "Base Metal" decreased imports on 22%;
- Affected sections of "Machinery and Electrical Eq." increased imports on 36%;
- Affected sections of "Vehicles" decreased imports on 12%;

## Impacts: External View
<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/external_impacts.png" alt="Alt text" width="800"/>

**Key takeaways:**
- Imports spiked in Q1 of 2025 but then decreased;
- Imports from Canada and China decreased;

## Impacts: Internal View
<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/internal_impacts.png" alt="Alt text" width="800"/>

**Key takeaways:**
- Commercial balance gap decreased and customs duties jumped 460%;
- Import Prices decreased slightly;
- Production Prices increased slightly;
- Industrial Production changed from
negative to positive trend;
- Manufacturing Employment continues todecrease while Unemployment Ratecontinues to increase;
 
## Machine Learning Model Process
**Goal:** Predict Consumer Price Index 2026-2027

**Inputs:**: Commercial Balance, Customs Duties, Import Price Index, Producer Price Index

**Process:**
1. **Extraction of historical data.** Range between 2015 and 2026;
2. **Conversion of series to Month-over-Month**;
3. **Creation of lag series.** 12 lags created for each series (1 -12 months);
4. **Hypothesis testing.** For each series was performed hypothesis testing to reject (or not) if the lag series had a significant impact on the dependable variable;
5. **Selection of features.** According to significance, correlation and amount of records. Commercial Balance and Customs Duties series were dropped (no impact found on CPI);
6. **ML algorithm testing** Best results (R2 score: 0.402) obtained with: GridSearch: Elastic Net, TimeSeriesSplit (5 splits), StandardScaler;
7. **Independent Variables Forecast.** Creation of 24 new periods using SARIMAX;
8. **Dependent Variable Forecast.** Application of best algorithm using full historic data as train and previous forecast as test.

## Estimates
<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/estimates.png" alt="Alt text" width="800"/>

**Key takeaways:**
- Commercial Balance and Duties don't influentiate Consumer Price;
- Import Price tends to zero with less volatility;
- Producer Price increases and stabilizes near 0;
- Consumer Prices will keep increasing at low rate;

## Scope Evaluation

In order to evaluate the scope of existing tariffs and its negative balance principle, the following rubric has been created:

<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/rubric1.png" alt="Alt text" width="800"/>

**Final score of 0.4 reflects a strategy partially/mostly on target**

## Policy Effect Assessment

In order to evaluate the effect of existing tariffs externally and internally, the following rubric has been created:

<img src="https://github.com/RVazSantos/AreTariffsMakingAmericaGreatAgain/raw/main/Images_Videos/Images/rubric2.png" alt="Alt text" width="800"/>

**Final score of 1.1 reflects a positive effect of the policies taken**

## Recommendations

Since the previous results show a positive effect, existing policies should be maintained and reinforced. Therefore, the following observations should be taken in consideration:

**Consider chinese computers and cellphones.** Chapter 8471: "Automatic data processing machines" and Chapter 8517: "Telephone sets" haven't been targeted yet. They are 4th and 5th from all chapters. Nearly 50% is produced in China.

**Consider Japanese cars.** Japan is the 5th biggest import partner mostly due to automotive and auto-parts imports. While specific tariffs are already implement, applying countrie specific tariffs can complement earlier actions. 

**Consider Vietnamese cellphones.** Vietnam is the 6th biggest import partner with the "telephone sets" being the primary chapter. Import values from Vietnam have increased 71% between 2020 and 2024.

**Reinforce Tariffs to Mexico.** Imports from Mexico keep increasing and Mexican pesos are losing value to USD making Mexican products even more competitive.

**Boost automatic data processing machines internal production.** Imports of this chapter keep increasing at a high pace (over 100% in 2025) showing a lack of internal production.

**Alternatives to Canadian Oil.** Petroleum oils are the 2nd biggest chapter and more than half is imported from Canada. Instead of imposing tariffs (because oil has a considerable effect on inflation), consider new sources or increases others.

## Warnings

**Reassess frequently!** Relevant time gap between the import of a product/raw material until its purchased by a final consumer. Most of the effects aren't covered by existing data. Also, new action should take this in consideration (preferable to wait before strengthen tariffs).

**High Customs Duties!** It's estate revenue, but later paid by consumers. Historical data didn't show effect between duties and CPI, but…duties have never been so high!  Average american went from paying 20$ to 90$ per month(hidden tax).

## Main challenges:

**Data Collection.** Collection techniques weren't very complex (dataset downloads and web scraping). The hardest part was to identify meaningful inputs, its sources and the most suitable view (e.g. YoY or MoM)

**Tariff Timeline** The year of 2025 was chaotic regarding tariff threats, implementations, suspensions, increases and decreases. Documentation of affected chapters in done mid text of pdf files.

**ML Model.** To target a macroeconomic indicator can be very complex because it's a time series that relies on a multitude of factors. Creation of lags can be complex and picking a view such as YoY proved to be a bad choice for ML. Needed to replace by MoM.

## Possible improvements:

**Reassess with more data.** In some months the effect of tariffs will be clear. Independent variables excluded from the ML Model (e.g. duties) can be proven to have a bigger correlation due to such high level unseen before.

**API connection.** All data gathered was downloaded, therefore its static. An API connection hasn't been created due to fees. However, to ensure a continuous data feed and allow in time monitoring, an API implementation would be a valuable addition.

**ML Model.** According to the scope of the project, the model took in consideration mostly trade variables. However, to better predict CPI other variables should be included (e.g. energy index, oil prices). Also, if duties keep being a non-factor, time range can be extended over the limit of duties (2015) for a more expressive historical data.

## Sources

- [UN Comtrade Database](https://comtradeplus.un.org/) This source aggregates detailed global annual and monthly trade statistics by product and trading partner.
- [US Treasury Fiscal Data](https://fiscaldata.treasury.gov/) Contains the total amount of customs duties collected over the years/months since 2015.
- [Federal Reserve Economic Data](https://fred.stlouisfed.org/)Source used to collect the following indicators: Import Price Index, Producer Price Index, Consumer Price Index, EUR/USD, MXN/USD, CNY/USD and CAD/USD
- [US Bureau of Labor Statistics](https://www.bls.gov/)Source used to collect the following indicators: Manufacturing Employment and Unemployment Rate.
- [Eurostat](https://ec.europa.eu/eurostat)Source used to collect European Union GDP.
- [INEGI](https://www.inegi.org.mx/default.html)Source used to collect Mexican GDP.
- [National Bureau of Statistics of China](https://data.stats.gov.cn/english/easyquery.htm?cn=B01)Source used to collect Chinese GDP.
- [Statistics Canada](https://www.statcan.gc.ca/en/start)Source used to collect Canadian GDP.
- [Federal Register](https://www.federalregister.gov/)Source used to download proclamations of steel, aluminum, automotive and auto parts.
- [Tax Foundation](https://taxfoundation.org/)Source used to support tariff timeline.
- [Reed Smith](https://www.reedsmith.com/)Source used to support tariff timeline.
- [C.H. Robinson](https://www.chrobinson.com/en-us/)Source used to support tariff timeline.
- [International Trade Administration](https://www.trade.gov/)Source used to support division of HS codes by chapters and sections.
- [European Commission](https://commission.europa.eu/index_en)Source used to support division of HS codes by chapters and sections.
- [Exporter.AI](https://exporterai.com/index.html)Source used to support division of HS codes by chapters and sections.
