# EV_Between_Adoption_and_Barriars
Washington has over 39.3 million registered vehicles, but only 6% of them are electric.This large gap highlights uneven EV adoption across the state and slows progress toward reducing emissions and transitioning away from ICE vehicles.
# Introduction: 
Washington State has more than 39.3 million registered vehicles, yet only 6% are electric.
This analysis explores the key factors affecting EV adoption across the state, including population distribution, income levels, political trends, and vehicle-use patterns.
By understanding these factors, we identify challenges, opportunities, and strategies to support a smoother transition from ICE vehicles to cleaner electric options.
# Problem Statement:
Washington has over 39.3 million registered vehicles, but only 6% of them are electric.
This large gap highlights uneven EV adoption across the state and slows progress toward reducing emissions and transitioning away from ICE vehicles.
# Approaches:
To better understand the factors influencing EV and hybrid adoption, the following analytical approaches were used:
1. Demographic Analysis
-	Compare population size across counties (high-population vs. low-population).
-	Identify how population correlates with electrification levels.
2. Political Leaning Assessment
-	Investigate whether counties with stronger Democratic or Republican votes adopt EVs differently.
-	Analyze vote distribution in the 2024 elections to compare with EV penetration.
3. Economic Indicators
-	Analyze median income by county.
-	Evaluate how higher income regions like King County correlate with EV uptake.
4. Vehicle Registration Analysis
-	Compare percentage of ICE, EV, and hybrid vehicles across counties.
-	Identify top brands and models for each vehicle type (ICE/EV/Hybrid).
-	Understand primary vehicle use and its impact on adoption.
5. Support Program Evaluation
-	Consider the effect of federal funds ($38M in 2024) on supporting EV infrastructure and incentives.
# Target Audience:
Washington State Department of Transportation (WSDOT) specifically Electrification & Sustainability Team Members
# Dataset:
Rows: around 40 M
Columns: 22
## Dataset Dictionary

| Field Name | Description | Column Name | Type |
|-----------|-------------|-------------|------|
| Transaction Month and Year | The month and year in which a transaction was recorded into Department of Licensing's computer system | start_of_month | Floating Timestamp |
| Make | Manufacturer of the vehicle (decoded from VIN) | make | Text |
| Model | Model of the vehicle (decoded from VIN) | model | Text |
| Model Year | Model year of the vehicle (decoded from VIN) | model_year | Number |
| Vehicle Color | Color of the vehicle (may be missing) | primary_color | Text |
| Vehicle Type | Category of vehicle based on physical appearance and/or intended use | vehicle_type | Text |
| Vehicle Primary Use | How the vehicle is registered to be used (similar to use class) | vehicle_primary_use | Text |
| Fuel Type Primary | Main source of power used to propel the vehicle | fuel_type_primary | Text |
| Fuel Type Secondary | Additional power source used to propel the vehicle | fuel_type_secondary | Text |
| Gross Vehicle Weight Rating Class | Numeric class (1–8) for max operating weight, typically used for trucks | gross_vehicle_weight_rating_class | Text |
| Gross Vehicle Weight Rating Range (lbs) | Weight range for maximum operating weight (in pounds); used for trucks | gross_vehicle_weight_rating_range | Text |
| Electrification Level | EV classification: Mild Hybrid, Strong Hybrid, PHEV, or EV | electrification_level | Text |
| Plate Background | Background on the issued license plate (standard or special) | plate_background | Text |
| Plate Configuration | Standard or personalized plate configuration | plate_configuration | Text |
| Owner Type | Indicates whether the vehicle is registered to individuals or a business | owner_type | Text |
| County | County of residence for the vehicle owner | county | Text |
| State | State of residence for the vehicle owner | state | Text |
| Postal Code | 5-digit USPS ZIP Code for the vehicle owner's residence | zip_code | Text |
| Transaction Type | Category of activity performed (registration action) | transaction_type | Text |
| Transaction Channel | How the transaction was performed (online, in-person, mail) | transaction_channel | Text |
| 2020 GEOID | Census 2020 geographic identifier (tract-level) | _2020_census_tract | Text |
| Transaction Count | Count of vehicle registration records in this row | vehicle_record_count | Number |

# Data handling:
Main data 
The cleaning was only in tableau where it was big data that Python didn’t handle it.
1.	Hide 6 rows in Tableau:
a.	vehicle color: a lot of Null, also not needed
b.	Gross Vehicle weight rating class: not needed
c.	 Gross Vehicle weight rating range: not needed
d.	 Postal Code: we have county and state, over information
e.	2020 GEOID: 
f.	Plate Background: not needed
2.	We have null in Fuel Type Secondary, and it is because not all Vehicle have An additional source of power.
3.	Change the type of model year to Date 
Other data 
Cleaning was in Excel 
# Limitations:
Data Availability
•	EV registration data may not capture vehicles registered out-of-state or recently purchased.
•	Some counties may have incomplete or outdated income or demographic records.
2. Correlation vs. Causation
•	While political leaning, income, and population correlate with EV adoption, they do not directly prove causation.
3. Rapid Market Changes
•	EV market conditions (prices, incentives, supply shortages) change quickly and may not be reflected in the analysis.
4. Infrastructure Variability
•	Charging infrastructure data may vary between public vs. private installations and may not reflect total access.
5. Behavioral Factors Not Captured
•	Individual preferences, brand loyalty, and personal driving habits are not directly reflected in the dataset. 
                         
# Recommendations:
Based on the findings, the following recommendations can enhance EV adoption:
1. Strengthen Infrastructure in Low-Adoption Counties
•	Expand charging stations in rural and low-population counties (e.g., Garfield, Wahkiakum).
•	Prioritize fast chargers along key commuting routes.
2. Incentivize Affordability
•	Provide targeted subsidies or tax credits for low-income households.
•	Encourage the availability of affordable EV models in rural dealerships.
3. Tailored Awareness Campaigns
•	Launch local awareness programs addressing misconceptions about EV range, reliability, and cost savings.
•	Create county-specific campaigns aligned with political and cultural attitudes.
4. Enhance Public-Private Partnerships
•	Collaborate with automakers and private companies to expand EV fleets.
•	Encourage workplaces to install charging points.
5. Data-Driven Policy Planning
•	Use county-level data to tailor state policies.
•	Prioritize counties showing the largest gap between ICE and EV registrations.
6. Promote Hybrid Vehicles as Transition Options
•	Position hybrids as an intermediate step for counties hesitant to adopt full EVs.

# Tools &amp: 
Tableau

# Future Improvements: 
-	Knowing the citizen’s behavior 
-	 See footprint effects for each type of vehicle 

# References
(n.d.). Retrieved from https://www.washingtonpolicy.org/publications/detail/results-of-washingtons-ev-instant-rebate?gad_source=1&gad_campaignid=21887239327&gbraid=0AAAAADbzGwEZuGCU3yr---QjoBM_kXsBd&gclid=CjwKCAiA_orJBhBNEiwABkdmjCQHX3gNBzpzueIoGRxLIox3WRv7XMvNZVsbtoktR2_LEiFcY
(n.d.). Retrieved from https://hdpulse.nimhd.nih.gov/dictionary.php#income
(n.d.). Retrieved from https://www.theepochtimes.com/bright/electric-vehicles-the-good-the-bad-and-the-ugly-2-post-5861200?utm_medium=DigitalMkt&utm_source=google&utm_campaign=PM_max-content_JaneAusten-mik-20251118&gl=reg&gad_source=1&gad_campaignid=23282724121&gbraid=0AAAAACvu
(n.d.). Retrieved from https://www.instituteforenergyresearch.org/regulation/washington-states-ev-rebate-program-is-costly-and-has-missed-its-expected-goals/?gad_source=1&gad_campaignid=22522217224&gbraid=0AAAAADhYN4EWSzpMwhAaNwkzElGXSFKB6&gclid=Cj0KCQiAoZDJBhC0ARIsAERP-F9rL5ho
(n.d.). Retrieved from https://www.kaggle.com/datasets/liamarguedas/washington-electric-vehicle-population/data
(n.d.). Retrieved from https://catalog.data.gov/dataset/vehicle-registrations-by-class-and-county
(n.d.). Retrieved from https://data.wa.gov/Transportation/Electric-Vehicle-Population-Size-History-by-County/q5qv-gkcz
(n.d.). Retrieved from https://hdpulse.nimhd.nih.gov/data-portal/social/map?age=001&age_options=ageall_1&demo=00011&demo_options=income_3&race=00&race_options=race_7&sex=0&sex_options=sexboth_1&socialtopic=030&socialtopic_options=social_6&statefips=53&statefips_options=area_sta
(n.d.). Retrieved from https://waevinstantrebates.org/program-results/
EVs — The Good, the Bad, and the Ugly (2025). [Motion Picture].
