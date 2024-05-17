# DATA

## Exploration and Transformations

### Dataset Overview

The dataset sourced from Kaggle was very clean and organized. Upon initial exploration, I identified 23 different features:

- `trans_date_trans_time`, `cc_num`, `merchant`, `category`, `amt`, `first`, `last`, `gender`, `street`, `city`, `state`, `zip`, `lat`, `long`, `city_pop`, `job`, `date_of_birth`, `trans_num`, `unix_time`, `merch_lat`, `merch_long`, `is_fraud`

### Feature Selection and Transformation

#### Initial Feature Selection

I initially selected the following features for my model:

- `dob`, `amt`, `zip`, `lat`, `long`, `city_pop`, `unix_time`, `merch_lat`, `merch_long`, `gender`

However, I later decided to remove the `gender` feature. Although it showed a high correlation, excluding it improved the model's predictive performance.

#### Feature Engineering

1. **Gender Feature Transformation**:
    - To encode the gender feature, I used the following code:
    ```python
    data_frame['gender'] = data_frame['gender'].apply(lambda x: 1 if x == "M" else 0)
    ```

2. **Date of Birth Transformation**:
    - I extracted the year from the `dob` feature, as the day and month were not useful for the model:
    ```python
    data_frame['dob_year'] = pd.DatetimeIndex(data_frame['dob']).year
    data_frame = data_frame.drop(columns=['dob'])
    ```

3. **Standard Scaling**:
    - To handle the different scales of the features, such as `unix_time`, I applied a `StandardScaler` to normalize the data:
    ```python
    from sklearn.preprocessing import StandardScaler

    scaler = StandardScaler()
    scaled_features = scaler.fit_transform(data_frame[['amt', 'zip', 'lat', 'long', 'city_pop', 'unix_time', 'merch_lat', 'merch_long', 'dob_year']])
    ```

4. **Handling Class Imbalance**:
    - To address the class imbalance in the dataset, I used the Synthetic Minority Over-sampling Technique (SMOTE), which significantly helped reduce overfitting:
    ```python
    from imblearn.over_sampling import SMOTE

    smote = SMOTE()
    X_resampled, y_resampled = smote.fit_resample(X, y)
    ```

### Summary

Through careful feature selection, transformation, and scaling, as well as addressing class imbalance, I was able to prepare the dataset for effective model training. These steps were crucial in enhancing the model's performance and reducing overfitting.

For more details, refer to the [DATA](DATA.md) file.
