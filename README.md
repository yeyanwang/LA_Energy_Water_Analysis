# Energy and Water Consumption Analysis for Buildings in LA
## Project Overview
Energy and water are essential components of our daily lives, playing a critical role in driving socio-economic progress, maintaining the balance of ecosystems, and ensuring human survival.

Analyzing historical usage data is a significant aspect of sustainable development. The primary objective of this project is to employ various statistical methods to analyze historical energy and water usage within the City of Los Angeles in order to understand how energy and water resources are utilized, identify patterns, and pinpoint any inefficiencies or anomalies in consumption. Additionally, this analysis will enable us to forecast future demand for these resources, allowing utilities and organizations to effectively plan and allocate resources to ensure a reliable supply that meets the needs of customers.

## Dataset 
The [dataset](https://dev.socrata.com/foundry/data.lacity.org/9yda-i4ya) for this project is provided by LA City's Existing Buildings Energy & Water Efficiency (EBEWE) Program. 

## Research Areas
We are interesting in discover: 
 1. What are the top five property types that exhibit the strongest correlation between Water Use and Carbon Emissions, as well as between Source Energy Use Intensity (Source EUI) and Carbon Emissions?
 2. What are the top ten property types demonstrate the highest energy and water usage per square footage among buildings constructed after the year 2000?
 3. Is there a correlation between Water Use and Gross Building Floor Area (GFA) for any specific property type, and if so, what is the nature of the relationship for the property type with the highest correlation value?
 4. In the case of multi-family housing buildings, is there a relationship between the year built and Source Energy Use Intensity (Source EUI), as well as between the year built and water use per square foot?

## Project Pipeline
1. **Data Collection:** Fetch data from Socratas by performing API calls
2. **Data Cleaning:** Convert data into correct data types, drop irrelavent columns and rows with `NaN` values
3. **Dataframe Serialization:** Transform the cleaned data into Pandas DataFrame format that can be stored and accessed later for analysis
4. **Data Visualization:** Create data visualization by utilizing scatter plots, bar graphs, and other graphical methods. Employ techniques such as fitting a line of best fit and calculating the coefficient of determination (R-squared) to identify trends and patterns within the data.

## Findings
 1. What are the top five property types that exhibit the strongest correlation between Water Use and Carbon Emissions, as well as between Source Energy Use Intensity (Source EUI) and Carbon Emissions?

    **Top 5 Property Types with the highest correlation between Water Use and Carbon Emissions**
    ![image](https://user-images.githubusercontent.com/116146774/215669260-c0e7c787-7a7a-4993-9e13-2533af04d319.png)

    **Top 5 Property Types with the highest correlation Source Energy Use Intensity (Source EUI) and Carbon Emissions**
    ![image](https://user-images.githubusercontent.com/116146774/215669494-b66baa13-d89f-4f76-b6c5-9036dc017026.png)


    ![image](https://user-images.githubusercontent.com/116146774/215670361-18ae311f-f76a-4342-8e04-756f824b1ceb.png)
    ![image](https://user-images.githubusercontent.com/116146774/215670404-ea348698-968e-4b55-8b4a-afc82434c2d9.png)
   
   For water use and carbon emissions, there appears to be a relatively strong positive correlation for Parking buildings, where the correlation coefficient between the two variables is 0.7173057056152874. For source energy use and carbon emissions, there appears to be a very strong positive correlation for Retail Stores, where the correlation coefficient between the two variables is 0.9830449798002524. It seems that CO2e have a stronger relationship to Source EUI and accordingly, the focus should be on reducing Source EUI to reduce carbon emissions.
 
2. What are the top ten property types demonstrate the highest energy and water usage per square footage among buildings constructed after the year 2000?

   **Property Types with the Highest Water Usage**
   ![image](https://user-images.githubusercontent.com/116146774/215670474-82749cbf-5251-482d-9687-6937b2f30ed5.png)

   **Property Types with the Highest Energy Usage**
   ![image](https://user-images.githubusercontent.com/116146774/215670522-b44eb78f-2d38-499f-ac67-3000a4cab5fb.png) 
   
   Hotel has the highest water consumption per sq-ft, with a value of 8115.6 kgal/sq-ft for building built after 2000. Medical Office has the highest energy consumption per sq-ft, with a value of 168.6 kgal/sq-ft for buildings built after 2000. Overall, new Hotels have high water and energy use and therefore, more measures should be taken to regulate energy and water consumption at new Hotels.
 3. Is there a correlation between Water Use and Gross Building Floor Area (GFA) for any specific property type, and if so, what is the nature of the relationship for the property type with the highest correlation value?

   ![image](https://user-images.githubusercontent.com/116146774/215670617-4aec34df-9d15-42f5-8321-760b8043ab93.png)

   **Gross Building Floor Area vs Water Use for Manufacturing/Industrial Plants**
   ![image](https://user-images.githubusercontent.com/116146774/215670684-9492eb7f-788c-4b9a-8354-eb79114bae1d.png)
   
   For water use and gross building floor area, there appears to be a moderately strong positive correlation for Manufacturing/Industrial Plants, where the correlation coefficient between the two variables is 0.5215937191397046. Also, based on the correlation values, the focus should be on adapting more water conservation and reduction strategies at larger Medical Offices, Manufacturing Plants and Mixed Use Properties.
 4. In the case of multi-family housing buildings, is there a relationship between the year built and Source Energy Use Intensity (Source EUI), as well as between the year built and water use per square foot?

   ![image](https://user-images.githubusercontent.com/116146774/215670726-89b6e0c4-0f75-49bd-921c-aae77ec6fae7.png)
   ![image](https://user-images.githubusercontent.com/116146774/215670759-fb49876b-29b1-493f-adbf-ba0a104a7bbf.png)
   
   The water usage intensity has decreased with year the property was built, however, no such trend is observed for energy use intensity. Accordingly, the city should start focusing on improving the energy usage trend or better understand why this trend hasn't changed.
   
## Credit
- Los Angeles Department of Building and Safety(LADBS) Existing Buildings Energy & Water Efficiency (EBEWE) Program 
- Socrata
