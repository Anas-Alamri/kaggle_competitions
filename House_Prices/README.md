# House Prices: Advanced Regression Techniques 

## Problem Statement

When we speak about home most people have an idea of what they want in a place called home.There are many features that contribute to the value of a house. In order to estimate the value of a home we will try and analyze the top features that has an effect on the house value.
We are aiming to create a prediction model that will analyze the features and give an overall prediction of the house value.This will give us the ability to predict a house value with only the features.

**This solution will contribute to solving many problems:**
- Any home buyer can have a value approximation of their dream house.
- The Real-estate agent will have an expected value of a house given it's features.
- Real-estate investors can have an idea about the most desired features that contibute to the properties value.

The data obtained has 79 explanatory variables describing (almost) every aspect of residential homes. The data was gathered in Ames, Iowa.We will analize the data,clean it,visulize it then fit it in a model to get a prediction of the expected `SalePrice` of the house.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|SalePrice|int64|train|The property's sale price in dollars. This is the target variable that you're trying to predict.|  
|MSSubClass|Object|train/test|The building class| 
|MSZoning|object|train/test|The general zoning classification|
|LotFrontage|float64|train/test|Linear feet of street connected to property|
|LotArea|int64|train/test| Lot size in square feet|
|Street|object|train/test|Type of road access|
|Alley|object|train/test|Type of alley access|
|LotShape|object|train/test| General shape of property|
|LandContour|object|train/test|Flatness of the property|
|Utilities|object|train/test|Type of utilities available|
|LotConfig|object|train/test|Lot configuration|
|LandSlope|object|train/test|Type of alley access|
|LotShape|object|train/test| Slope of property|
|Neighborhood|object|train/test|Physical locations within Ames city limits|
|Condition1|object|train/test|Proximity to main road or railroad|
|Condition2|object|train/test|Proximity to main road or railroad (if a second is present)|
|BldgType|object|train/test|Type of dwelling|
|HouseStyle|object|train/test|Style of dwelling|
|OverallQual|int64|train/test|Overall material and finish quality)|
|OverallCond|object|train/test|OverallCond|
|YearBuilt|int64|train/test|Original construction date|
|BuildingAge|int64|train/test|Age of the building|
|RemodelAge|int64|train/test|number of years since last remodel|
|YearRemodAdd|int64|train/test|Remodel date|
|RoofStyle|object|train/test|Type of roof|
|RoofMatl|object|train/test|Roof material|
|Exterior1st|object|train/test|Exterior covering on house|
|Exterior2nd|object|train/test|Exterior covering on house (if more than one material)|
|MasVnrType|object|train/test|Masonry veneer type|
|MasVnrArea|int|train/test|Masonry veneer area in square feet|
|ExterQual|object|train/test|Exterior material quality|
|ExterCond|object|train/test|Present condition of the material on the exterior|
|Foundation|object|train/test|Type of foundation|
|BsmtQual|object|train/test|Height of the basement|
|BsmtCond|object|train/test|General condition of the basement|
|BsmtExposure|object|train/test|Walkout or garden level basement walls|
|BsmtFinType1|object|train/test|Quality of basement finished area|
|BsmtFinSF1|float64|train/test|Type 1 finished square feet|
|BsmtFinType2|object|train/test|Quality of second finished area (if present)|
|BsmtFinSF2|float64|train/test|Type 2 finished square feet|
|BsmtUnfSF|float64|train/test|Unfinished square feet of basement area|
|TotalBsmtSF|float64|train/test|Total square feet of basement area|
|Heating|object|train/test|Type of heating|
|HeatingQC|object|train/test|Heating quality and condition|
|CentralAir|object|train/test|Central air conditioning|
|Electrical|object|train/test|Electrical system|
|1stFlrSF|int64|train/test|First Floor square feet|
|2ndFlrSF|int64|train/test|Second floor square feet|
|LowQualFinSF|object|train/test|Low quality finished square feet (all floors)|
|GrLivArea|int64|train/test|Above grade (ground) living area square feet|
|BsmtFullBath|float64|train/test|Basement full bathrooms|
|BsmtHalfBath|float64|train/test|Basement half bathrooms|
|FullBath|int64|train/test|Full bathrooms above grade|
|HalfBath|int64|train/test|Half baths above grade|
|BedroomAbvGr|int64|train/test|Number of bedrooms above basement level|
|KitchenAbvGr|int64|train/test|Number of kitchens|
|KitchenQual|object|train/test|Kitchen quality|
|TotRmsAbvGrd|int64|train/test|Total rooms above grade (does not include bathrooms)|
|Functional|object|train/test|Home functionality rating|
|Fireplaces|int64|train/test|Number of fireplaces|
|FireplaceQu|object|train/test|Fireplace quality|
|GarageType|object|train/test|Garage location|
|GarageYrBlt|int|train/test|Year garage was built|
|GarageFinish|object|train/test|Interior finish of the garage|
|GarageCars|object|train/test|Size of garage in car capacity|
|GarageArea|object|train/test|Size of garage in square feet|
|GarageQual|object|train/test|Garage quality|
|GarageCond|object|train/test|Garage condition|
|PavedDrive|object|train/test|Paved driveway|
|WoodDeckSF|int|train/test|Wood deck area in square feet|
|OpenPorchSF|int|train/test|Open porch area in square feet|
|EnclosedPorch|object|train/test|Enclosed porch area in square feet|
|3SsnPorch|int|train/test|Three season porch area in square feet|
|ScreenPorch|int|train/test|Screen porch area in square feet|
|PoolArea|int|train/test|Pool area in square fee|
|PoolQC|object|train/test|Pool quality|
|Fence|object|train/test|Fence quality|
|MiscFeature|object|train/test|Miscellaneous feature not covered in other categories|
|MiscVal|int|train/test|Screen porch area in square feet|
|PoolArea|int|train/test|Pool area in square fee|
|PoolQC|object|train/test|Pool quality|
|Fence|object|train/test|Fence quality|
|MiscVal|int64|train/test|Value of miscellaneous feature|
|MoSold|int64|train/test|Month Sold|
|YrSold|int64|train/test|Year Sold|
|SaleType|object|train/test|Type of sale|
|SaleCondition|object|train/test|Condition of sale|
