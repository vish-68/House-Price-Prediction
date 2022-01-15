
# House Price Prediction

There are a number of factors which determine property prices, some are logical, based on economic theories and population density and some are based on more intangible factors, like availability of amenities & necessities, neighborhood, etc. 
Build a linear regression model with stochastic gradient descent to predict the price of the property from the dataset having attributes such as sale type, sale condition etc. 

## Data Analysis

In Mental-Or-Physical-Disease-Treatment dataset we are provided 80 features(including target 
variable) and 2194 records.

* SalePrice - the property's sale price in dollars. This is the target variable that you're trying to predict.
* MSSubClass: The building class
* MSZoning: The general zoning classification
* LotFrontage: Linear feet of street connected to property
* LotArea: Lot size in square feet
* Street: Type of road access
* Alley: Type of alley access
* LotShape: General shape of property
* LandContour: Flatness of the property
* Utilities: Type of utilities available
* LotConfig: Lot configuration
* LandSlope: Slope of property
* Neighborhood: Physical locations within Ames city limits
* Condition1: Proximity to main road or railroad
* Condition2: Proximity to main road or railroad (if a second is present)
* BldgType: Type of dwelling
* HouseStyle: Style of dwelling
* OverallQual: Overall material and finish quality
* OverallCond: Overall condition rating
* YearBuilt: Original construction date
* YearRemodAdd: Remodel date
* RoofStyle: Type of roof
* RoofMatl: Roof material
* Exterior1st: Exterior covering on house
* Exterior2nd: Exterior covering on house (if more than one material)
* MasVnrType: Masonry veneer type
* MasVnrArea: Masonry veneer area in square feet
* ExterQual: Exterior material quality
* ExterCond: Present condition of the material on the exterior
* Foundation: Type of foundation
* BsmtQual: Height of the basement
* BsmtCond: General condition of the basement
* BsmtExposure: Walkout or garden level basement walls
* BsmtFinType1: Quality of basement finished area
* BsmtFinSF1: Type 1 finished square feet
* BsmtFinType2: Quality of second finished area (if present)
* BsmtFinSF2: Type 2 finished square feet
* BsmtUnfSF: Unfinished square feet of basement area
* TotalBsmtSF: Total square feet of basement area
* Heating: Type of heating
* HeatingQC: Heating quality and condition
* CentralAir: Central air conditioning
* Electrical: Electrical system
* 1stFlrSF: First Floor square feet
* 2ndFlrSF: Second floor square feet
* LowQualFinSF: Low quality finished square feet (all floors)
* GrLivArea: Above grade (ground) living area square feet
* BsmtFullBath: Basement full bathrooms
* BsmtHalfBath: Basement half bathrooms
* FullBath: Full bathrooms above grade
* HalfBath: Half baths above grade
* Bedroom: Number of bedrooms above basement level
* Kitchen: Number of kitchens
* KitchenQual: Kitchen quality
* TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)
* Functional: Home functionality rating
* Fireplaces: Number of fireplaces
* FireplaceQu: Fireplace quality
* GarageType: Garage location
* GarageYrBlt: Year garage was built
* GarageFinish: Interior finish of the garage
* GarageCars: Size of garage in car capacity
* GarageArea: Size of garage in square feet
* GarageQual: Garage quality
* GarageCond: Garage condition
* PavedDrive: Paved driveway
* WoodDeckSF: Wood deck area in square feet
* OpenPorchSF: Open porch area in square feet
* EnclosedPorch: Enclosed porch area in square feet
* 3SsnPorch: Three season porch area in square feet
* ScreenPorch: Screen porch area in square feet
* PoolArea: Pool area in square feet
* PoolQC: Pool quality
* Fence: Fence quality
* MiscFeature: Miscellaneous feature not covered in other categories
* MiscVal: $Value of miscellaneous feature
* MoSold: Month Sold
* YrSold: Year Sold
* SaleType: Type of sale
* SaleCondition: Condition of sale
## Approach

Our Main goal is to know that whether which applicant 
it belong to defaulter or non-defaulter.

* Data Exploration : Exploring dataset using pandas,numpy,matplotlib and seaborn.
* Model Selection I : Tested all base models to check the base accuracy. Also ploted and calculate Performance Metrics to check whether a model is a good fit or not.
* Model Selection II : After testing all base if some of them are not working properly then we have to do model tunning
* Pickle File : Selected model as per best accuracy and created pickle file using pickle library.
* Webpage & deployment : Created a webform that takes all the necessary inputs from user and shows output. After that I have deployed project on Herokuapp 

## Technologies Used

* Jupyter notebook, Spyder, VScode Is Used For IDE.
* For Visualization Of The Plots Matplotlib , Seaborn Are Used.
* Git Hub Is Used As A Version Control System.
* os is used for creating and deleting folders.
* csv is used for creating .csv format file.
* numpy is for arrays computations and mathematical operations
* pandas is for Manipulation and wrangling structured data
* scikit-learn is used for machine learning tool kit
* pickle is used for saving model
* LinearRegression is used for Linear Regression Implementation
* Ridge is used for Ridge Regression Implementation
* Lasso is used for Lasso Regression Implementation
* statsmodels.formula.api is used for Stats model Implementation
* SGDRegressor is used for SGD Implementation
* KNeighborsRegressor is used for KNN Implementation
* DecisionTreeRegressor is used for Decision Tree Implementation
* RandomForestRegressor is used for Random Forest Implementation
* SVR is used for SVM Implementation
* KFold validation is used for KFold Implementation
* VotingRegressor is used for Ensemble modelling Implementation

## Conclusion
We have developed model which is cpable to predict price of house by giving input
like which locality, size, and other features of house.
In this dataset we have 80 features(including target variable). First step 
is to import dataset, after importing dataset we have to check datatype of all
columns and missing values. We have to treat missing value according to their respective 
datatype. If it is categorical column we have to replace by mode, if it numerical column 
then we have to replace it by mean. In this case we have to check 
the categorical variable which mean how many categories are present
and perform same operation on train as well as test file and after that we 
have to treat missing values and after treating missing values.

Once missing values is treated next step we have to perform is 
data visualization in that we have to check for outliers and check 
whether the data is imbalanced or not.
Here we found outliers in many variable so we treat them one by one 
after that We have to delete some variable using domain knowledge and 
some using corelation plot.
Once all this steps are done we have to convert categorical values 
into numerical values for this we have to concat both the dataset i.e.
train and test dataset and we have to use dummy variable technique for 
converting categorical in to numerical values. And then again split 
train and test dataset in train dataset and test dataset.

For model selection we have to split train dataset into train and validation data
using train test split function before going to this step, First Wehave to perform
StandardScalar After all this done we have to build model we build several models like 
Linear Regression, Ridge Regression, Lasso Regression, OLS stats model,
SGDRegressor, KNeighborsRegressor, DecisionTreeRegressor, RandomForestRegressor ,
SVR, KFold validation, VotingRegressor(Ensemble modelling) out of all 
I got Ensemble modelling as good model with 88% of accuracy and K-fold as 84%. 
And ensemble model you can save using pickle file.

After this we have to perform this on test dataset after scaling data 
we do not have to train model again only use predict function on it and get the output and submit it.