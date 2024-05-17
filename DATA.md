# DATA

## Exploration and Trasformations

* The dataset that I got from Kaggle was very clean and organized, when doing my first exploration of the dataset I would find that there would be 23 different features which would include: 
    * trans_date_trans_time, cc_num, merchant, category, amt, first, last, gender, street, city, state, zip, lat, long, city_pop, job, date_of_birth, trans_num, unix_time, merch_lat, merch_long, and is_fraud.
    
* I would first choose the features ['dob', 'amt', 'zip', 'lat', 'long', 'city_pop', 'unix_time', 'merch_lat', 'merch_long', 'gender'], later I would get rid of the gender feature. The gender feature would give me a high correlation but when I took the feature the model would start predicting better:
    * To change the gender feature I would use 
    ```
    data_frame['gender'] = data_frame['gender'].apply(lambda x: 1 if x == "M" else 0)
    ```

* I would also need to change the DOB feature to only get the year since the day and month are kind of useless:
    * To change the DOB feature I would use:
    ```
    data_frame['dob_year'] = pd.DatetimeIndex(data_frame['dob']).year
    data_frame = data_frame.drop(columns=['dob'])
    ```
    
* I would also use a StandarScaler for my models because many of my features would have entries over different types such as the unix time having so many diffent instances

* I would also use Synthetic Minority Over-sampling Technique (SMOTE) to help with the imbalance of the classes in my dataset which would help a lot with the overfitting problem that was in my dataset.
    