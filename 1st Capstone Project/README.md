<b>Introduction</b>

High air pollution levels have been consistently documented as a major environmental risk to health. Not only is air pollution a documented health risk, it is associated with an increased utilization of health care services. 

Given the health risks involved in elevated levels of air pollutants, it would be useful for health care providers and hospitals to predict the uptick of services during periods of poor air quality. Prediction of periods of increased patient illness could help with planning for hospital staffing needs as well as preventative care and messaging to reduce hospital visits. 

The hypothetical client in this case is Kaiser Permanente, a large managed care organization that runs a number of hospitals and clinics with an emphasis on preventive care and population health management. Prediction of air quality incidents that may affect population health and cause a spike in emergency room visits and hospitalizations may help Kaiser staff their clinics accordingly and in advance rather than face nursing shortages that could impact quality of care, wait times or their quality metrics.

<b>Analysis</b>

Air pollution data from the Environmental Protection Agency and weather data from the National Oceanic and Atmospheric Administration were collected and combined for this project. The data for 7 of the largest 10 cities in the United States was used to develop the predictive model; this subset consisted of 15 years of data (January 1, 2000 through December 31, 2015) with both pollution and weather components.  These cities were New York, Los Angeles, Houston, Phoenix, Philadelphia, San Diego, and Dallas. This constitutes a dataset of 56,073 observations with 27 columns. 

For each pollutant, a logistic regression model was built to predict Air Quality Index outcome based on a set of features (Average Temperature, Maximum Temperature, Minimum Temperature, Elevation, Average Relative Humidity, Average Dew Point Temperature, Sunrise, Sunset, Average Station Pressure, Average Sea Level Pressure, and Sustained Wind Speed).

A number of model improvement feature importance steps were performed.  Utilizing the abbreviated list of features identified as most important to prediction of the outcome variable, logistic regression with cross-validation was performed again to finalize the modeling.  With a reduction from 11 to only 4-5 features, the reduced models still perform reasonably well without a drastic loss in accuracy or AUC.

<b>Client Recommendations</b>

Based on the analysis presented, recommendations could be made to Kaiser Permanente in several areas:
* Prevention
  * Population Health Management
  * Management of high risk patients
* Staffing
  * Hospital and Emergency Room
  * TeleHealth

Taken together, these initiatives have the potential to increase cost savings while improving patient care.  One recent example (American Journal of Accountable Care 2017) at Denver Health, a smaller managed care organization, evaluating the usage of population health strategies and predictive modeling to match resourcing with patient needs demonstrated $15.8 million savings over 26 months.  A larger organization such as Kaiser Permanente could yield significant savings through increased usage of predictive modeling to address patient health needs.

<b>Future Work</b>

Two specific areas could help expand the utility of this analysis:
* Inclusion of emergency room visits and hospital admissions for respiratory diseases in order to better predict the actual increase in illness caused by pollutant levels.  Unfortunately, the only available data through free sources was monthly/annual rates of hospital/ER visits, which do not provide the granularity necessary to make accurate predictions.
* It would be interesting to evaluate weather data leading up to any given day and determine how influential that is on pollutant levels, including if a rolling 3-day average is a better predictor and how large the window of influence is.

