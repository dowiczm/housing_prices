## Problem Statement

As a Data-Scientist for Zillow, my team is working on the production of a built-in feature meant to recommend a “fair” sale price for potential home-sellers. My role is to construct a linear-model that will run the back end operations of the feature, which will receive inputs manually entered by the prospective home-seller, to produce said recommendation. 
 
 
 ### Background Info

Selling a house can be a stressful experience. Many factors come into play when assessing a home's price, some of which, the home-seller may be unaware of. This project will be focused on identifying features that contribute to the price of a home, and putting them to work to construct a robust linear-model capable of predicting a fair sell-price for the Ames, Iowa area. The model will be tested on testing data unseen by the model during its creation.  


### Data Description 

The data used to create this model was sourced from (https://www.kaggle.com/c/dsir-222-ames-competition/data).
It contains information on 2,051 homes, and each homes 81 attributes along with its sale-price. The testing data was also sourced from (https://www.kaggle.com/c/dsir-222-ames-competition/data) and contains the same 81 attributes on 878 homes, with the final sale price absent. 

* [`train.csv`](./datasets/test.csv): Training Data
* [`test.csv`](./datasets/train.csv): Testing Data


### Data Dictionary

A full data dictionary can be found at (http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).


### Outside Research 

According to an article (https://www.opendoor.com/w/blog/factors-that-influence-home-value), there are 8 critical factors associated with influencing the price of a home. Many of these factors are economical, such as current interest rates and inventory, while others are relate to the homes specific attributes like age, condition, usable space, amenities and upgrades. This information was noted and taken into account while performing EDA.  

### EDA Results

- The factors identified through my EDA to include in the model are as follows:
    - Overall_Qual, Total_Bsmt_Sf, 1st_Flr_Sf, 2nd_Flr_Sf, Gr_Liv_Area, Full_Bath, Fireplaces, Garage_Area,
    - Totrms_Abvgrd, Lot_Area, Bldg_Type, Exter_Cond, Fence,

### Conclusions

- The final model had an R2_score of 0.8977 on the training data, and a RMSE of 26,121. These results imply the model is relatively robust, and on average miscalculated the sale-price of a home by 26,121. 

- The model is uninterpretable as the elements have been engineered using a polynomial function, standard scaler, and Lasso'd out. However, the result itself is very interpretable, and as a home-seller, could be used to predict a fair sale-price. 

- A linear-model holds all outside noise constant. Therefore, location, interest rates, and market inventory are not accounted for in the model. These are things the home-seller would have to account for themselves.

- I would not consider the model ready for imlementation. More data, feature engineering and testing would have to be done in later iterations to prep the model for real-world use.   
    

    

