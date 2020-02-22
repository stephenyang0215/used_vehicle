# Used Car Market Data Analysis
### Introduction
The objective of this side project is to examine the model forecasting of the used car listing price in the U.S.  
We had been searching for any possible dataset provided on the Internet, but those we found were not valuable enough to take into consideration. Most of them were with millions of rows but roughly with only four or five columns, or the periods were obsolete.
Thus, the qualifications of this sideproject's dataset are obvious.   
The vehicles information must be as precise and detailed as possible which means the quantity of the columns. Also the dataset better not be obsolete which means the dataset should be made in around 2019.  
Then, we decided to scrap the vehicle selling information posted on the usedcar websites.
Finally, here is the dataset we got which was made in 12/20/2019.  
| Number of Rows | Number of Columns |
| ------------- | ------------- |
|   2375350 |      29 |  

Below is the list of columns and its description:  
* CarID  
ID Number of each vehicle.  
* MakeId  
ID Number of each vehicle brand.  
* Title  
Title of vehicle.  
* Make   
Vehicle brand.  
* Model  
Vehicle Model.  
* Trim  
A vehicle trim model is a version of a vehicle model used by manufacturers to identify a vehicle's level of equipment.
* BodyStyle  
The body style of a vehicle refers to the shape and model of a particular automobile make.  
* Rental  
Tell if the vehicle is a rental car or not.  
* Location  
State and city/county of a vehicle where it located.  
* GasMileage_city  
Fuel efficiency in city area.  
* GasMileage_highway  
Fuel efficiency in highway.  
* Price
price of vehicle in USD.  
* Mileage  
One indicator of vehicle condition, a number of miles a vehicle covered.  
* Transmission  
A transmission is a machine in a power transmission system, which provides controlled application of the power.  
* FuelType  
Type of fuel that is used to provide power to vehicle.  
* ExteriorColor  
Color of exterior part of car.  
* InteriorColor  
Color of interior part of car.  
* DoorsNum  
Number of doors of car.  
* MaximumSeating  
Maximum number of seating.  
* Engine  
An engine is a machine designed to convert one form of energy into mechanical energy.  
* Drivetrain  
The drivetrain of a motor vehicle is the group of components that deliver power to the driving wheels.  
* VIN  
Vehicle Identification Number. VIN is used to identify a specific vehicle.  
* OptionCount  
Count of options on a car.  
* MajorOptions  
MajorOptions shows the major packages or equipment that a car uses.  
* Certified  
This column specify if a car is CPO(certified pre-owned). A CPO car comes with a complete inspection that repairs any damaged or worn parts before being offered for sale.  
* Accident Check  
Inspection of accidents occured on a car.  
* OwnershipHistory  
History of ownership of a car.  
* SellingDays  
Days of a car listed on the website.  
* OriginPrice  
Price offered by seller in the first place.  

[Data Exploration](Data_Cleaning_and_EDA.ipynb)(Click the link for further detail!) : Explore the dataset and check its distribution at multiple aspects.   
1. Distribution of each brand model marketshare and it's average price.  
![exp1](Images/vehicle_count.png)
2. Detection of top 30 models' price outliers.  
![exp2](Images/vehicle_boxplot.png)
3. Comparison of median income and average vehicle price of each state.  
![exp3](Images/State_income_price.png)
4. Median price comparison by body style over three grouped states by median income range.  
![exp4](Images/bodystyle_price_state.png)
5. Comparison of each body style by marketshare percentage and average vehicle price by three grouped states. 
![exp5](Images/bodystyle_price_percentage.png)

[Machine Learning](Usedcar_ML.ipynb)(Click the link for further detail!) : The task of ML is to fit the model to the dataset.
And find the optimal solution to the predication.     
### XGBoost
![ML1](Images/gbtree_train_test.png)  
method:gbtree
| R-squared | RMSE |
| ------------- | ------------- |
|   0.937 |      2650 |    
### Random Forest
![ML2](Images/RF_score.png)  
method:regression
| R-squared | RMSE |
| ------------- | ------------- |
|   0.94 |      2618 |

