# Streaming OTT  Subscription

For this analysis, we'll be examining customer churn data from a leading subscription-based streaming service. This industry giant boasts a vast library of movies, TV shows, and original content. Understanding why customers discontinue their subscriptions will be crucial in optimizing the user experience, reducing churn, and maximizing customer lifetime value.

# flowchart of Project
![STREAMING OTT PROJECT FLOWCHART (2)](https://github.com/user-attachments/assets/e7e8b1e2-aa06-4965-936c-2c4c078ab0c2)


# Exploration

## Statistics

### Numerical Features

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>AccountAge</th>
      <th>MonthlyCharges</th>
      <th>TotalCharges</th>
      <th>ViewingHoursPerWeek</th>
      <th>AverageViewingDuration</th>
      <th>ContentDownloadsPerMonth</th>
      <th>UserRating</th>
      <th>SupportTicketsPerMonth</th>
      <th>WatchlistSize</th>
      <th>Churn</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
      <td>243787.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>60.083758</td>
      <td>12.490687</td>
      <td>750.741017</td>
      <td>20.502179</td>
      <td>92.264061</td>
      <td>24.503513</td>
      <td>3.002713</td>
      <td>4.504186</td>
      <td>12.018508</td>
      <td>0.181232</td>
    </tr>
    <tr>
      <th>std</th>
      <td>34.285143</td>
      <td>4.327613</td>
      <td>523.073273</td>
      <td>11.243753</td>
      <td>50.505243</td>
      <td>14.421174</td>
      <td>1.155259</td>
      <td>2.872548</td>
      <td>7.193034</td>
      <td>0.385211</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>4.990000</td>
      <td>4.991154</td>
      <td>1.000065</td>
      <td>5.000547</td>
      <td>0.000000</td>
      <td>1.000007</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>30.000000</td>
      <td>8.740000</td>
      <td>329.147027</td>
      <td>10.763953</td>
      <td>48.382395</td>
      <td>12.000000</td>
      <td>2.000853</td>
      <td>2.000000</td>
      <td>6.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>60.000000</td>
      <td>12.500000</td>
      <td>649.878487</td>
      <td>20.523116</td>
      <td>92.249992</td>
      <td>24.000000</td>
      <td>3.002261</td>
      <td>4.000000</td>
      <td>12.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>90.000000</td>
      <td>16.240000</td>
      <td>1089.317362</td>
      <td>30.219396</td>
      <td>135.908048</td>
      <td>37.000000</td>
      <td>4.002157</td>
      <td>7.000000</td>
      <td>18.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>119.000000</td>
      <td>19.990000</td>
      <td>2378.723844</td>
      <td>39.999723</td>
      <td>179.999275</td>
      <td>49.000000</td>
      <td>4.999989</td>
      <td>9.000000</td>
      <td>24.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Categorical Features



<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SubscriptionType</th>
      <th>PaymentMethod</th>
      <th>PaperlessBilling</th>
      <th>ContentType</th>
      <th>MultiDeviceAccess</th>
      <th>DeviceRegistered</th>
      <th>GenrePreference</th>
      <th>Gender</th>
      <th>ParentalControl</th>
      <th>SubtitlesEnabled</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
      <td>243787</td>
    </tr>
    <tr>
      <th>unique</th>
      <td>3</td>
      <td>4</td>
      <td>2</td>
      <td>3</td>
      <td>2</td>
      <td>4</td>
      <td>5</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>top</th>
      <td>Standard</td>
      <td>Electronic check</td>
      <td>No</td>
      <td>Both</td>
      <td>No</td>
      <td>Computer</td>
      <td>Comedy</td>
      <td>Female</td>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>freq</th>
      <td>81920</td>
      <td>61313</td>
      <td>121980</td>
      <td>81737</td>
      <td>122035</td>
      <td>61147</td>
      <td>49060</td>
      <td>121930</td>
      <td>122085</td>
      <td>122180</td>
    </tr>
  </tbody>
</table>
</div>



## Analysis


### Churn Rate

![output_26_0](https://github.com/user-attachments/assets/de4a42b4-e84e-4d83-a032-941fb2f0c00b)

- Not Churned Customer - 81.88%
- Churned Customer - 18.12%

### Churn by Gender
![output_29_0](https://github.com/user-attachments/assets/32469a2c-f954-43e0-8d6d-cde9cd20bfe3)

- **Churn and Gender**-
    Among our users, there are more females than males. However, the churn rate for male users is slightly higher than the churn rate for female users.

### Account Age

![output_32_0](https://github.com/user-attachments/assets/cc396bc1-3eb7-44f6-8a0b-26569f3019cf)

    
![output_33_0](https://github.com/user-attachments/assets/2be4afcd-360e-4f1b-94d7-21122222afb4)

1. **User Age and Churn:**
   - Older users are more prevalent than new users.
   - Churn tends to be higher among accounts with lower age (newer users).
   - As account age increases, the churn rate decreases.

2. **Account Age Statistics:**
   - Median account age: 60 months
   - Highest account age: 120 months

3. **Churn Rates:**
   - Churn rate for new users (low account age): ~32%
   - Churn rate decreases to ~7% as account age increases.

### Total Monthly Charges
    
![output_36_0](https://github.com/user-attachments/assets/c3ddc056-14cb-4a9b-a5af-f3d6939851da)
    
1. **Churn and Monthly Charges:**
   - Churn rates tend to increase as monthly charges increase. Users with higher monthly charges are more likely to churn.
   - Low churn occurs when monthly charges are low.

2. **Subscription Distribution:**
   - There's a relatively high number of low monthly subscriptions, gradually decreasing toward higher subscription tiers.

3. **Monthly Charge Statistics:**
   - Minimum monthly price: 4.99
   - Maximum monthly price: 19.99

### Viewing Hours Per Week
![output_39_0](https://github.com/user-attachments/assets/905ca61b-4d03-4554-9b57-a6a978832343)

1. **Churn and Viewing Hours:**
   - Users with higher weekly viewing hours are less likely to churn compared to those with lower viewing hours.
   - High churn occurs among users who view less than or equal to four hours.
   - Users with viewing hours between 30 and 40 exhibit relatively stable churn.

2. **Viewing Hours Statistics:**
   - Average weekly view hours: 20.5
   - Minimum weekly view hours: 1
   - Maximum weekly view hours: 40

### Average Viewing Duration

![output_42_0](https://github.com/user-attachments/assets/a71cc22b-c2b9-493f-a4b8-ad1ee92c2708)


1. **Churn and Average View Duration:**
   
   - Users which have the low average view duration are more likely to churn than the users which have high average duration.
   - High churn occurs when the average view duration upto 40.
   - there is gradually decrease in churn rate from 50
   - Users with viewing hours between 125 and 175 exhibit relatively stable churn.
    
2. **Average view Duration Statistics :**

   - Minimum is 5.
   - Maximum is 179.99
   - Average is 92.37.

### Content Downloads Per Month
![output_45_0](https://github.com/user-attachments/assets/42256c7a-f96b-4d14-a69f-3952a7a0a063)
    
1. **Churn and Content Downloads Per Month:**
   - Users with high Content Downloads Per Month are more likely to churn compared to users with low Content Downloads Per Month.
   - The sudden drop of up to 50% in some bars indicates that people download new series and shows when they are released.
   - Users with high download activity likely subscribe to download new content.
   - High churn occurs when the download count exceeds 10.
   - There is a decrease in churn rate as the download count decreases.
   - Users with download counts between 30 and 50 exhibit relatively stable churn behavior.
   - Some users do not download shows or movies, possibly due to device limitations or a preference for watching on TV.

2. **Average View Duration Statistics:**
   - Minimum view duration is 0.
   - Maximum view duration is 49.
   - The average view duration across users is 24.48.

### User Rating
![output_48_0](https://github.com/user-attachments/assets/ac6b8ab4-a7dc-4875-8c5c-e487b7c6cb46)
    
1. **Churn and User Rating:**
   
   - There is no relationship between rating and churn because rating 1 to 5 there is relatively stable churn.
   - OTT streaming get relatively equal ratings.
    
2. **User Rating Statistics :**

   - Minimum is 1.
   - Maximum is 4.99
   - Average is 3.002.

### Support Ticket Per month

![output_51_0](https://github.com/user-attachments/assets/dc6fe519-10ac-4bc1-a3ba-e14e789195d6)


1. **Churn and Support Ticket:**
   
   - From the illustration, it shows that the higher the ticket generate, the users most likely to churn
- there is significantly low churn rate when there is no ticket generated. but when the ticket generated it also increaes the churn rate. 
   - Most churn rate are when the ticket generated 6 to 8.
    
2. **Support Ticket Statistics :**

   - Minimum is 0.
   - Maximum is 9.99
   - Average is 4.5.002.

### Watch List Size

![output_54_0](https://github.com/user-attachments/assets/84b0ea28-2bcd-4eb1-a0b2-927070855ddb)
    

1. **Churn and Watch List Size:**
   
   - There is no relationship between Watchlist and churn because there is relatively stable churn.
    
2. **User Rating Statistics :**

   - Minimum is 0.
   - Maximum is 24.99
   - Average is 12.02.

### Churn by Subscription
    
![output_57_0](https://github.com/user-attachments/assets/ff88e71c-2d23-427b-b646-a29c5a88c3db)

1. **Churn Rate by Subscription Type**:
   - The churn rate is highest among Basic subscribers, followed by Standard and Premium.
   - Specifically, users who subscribe to the Basic plan tend to have a higher churn rate.

2. **Premium Subscribers**:
   - Premium subscribers exhibit the lowest churn rate across all subscription types.
   - This suggests that Premium subscribers are more likely to stay with the service.

3. **User Preferences**:
   - Most users prefer the Premium subscription, followed by Standard and then Basic.


### Payment Method and Paperless Billing

![output_61_0](https://github.com/user-attachments/assets/34be1c57-cf87-4ee1-8c0a-ce72031aa49a)

1. **Churn and Payment Method:**
   
    - from this illustration, Users with electronic check have the higher churn rate followed by mail check  and bank transfer and credit.
    - Paperless billing affecting the churn rate is relatively very low.
3. **Overall Insights:**

    - users with Payment method which takes time and effort have thr highest churn rate as compared to the payment method that require less effort.


![output_63_0](https://github.com/user-attachments/assets/1822a2d7-a021-4950-93a8-ccdb009cf2a3)
    


1. **Churn and Paperless Billing**:
   - The diagonal represents the correlation of each variable with itself (which is always 1.0).
   - The off-diagonal values represent the correlation between `Churn` and `PaperlessBilling`.
   - When `PaperlessBilling` is `No`, the correlation with `Churn` is approximately -0.98, indicating a strong negative relationship. Customers who are not on paperless billing tend to have lower churn rates.
   - Conversely, when `PaperlessBilling` is `Yes`, the correlation with `Churn` is around -0.91. This suggests that customers on paperless billing have a slightly higher churn rate.

2. **Overall Insights**:
   - Paperless billing appears to be an important factor affecting churn behavior.
   - Customers who prefer paperless billing are more likely to churn.
   - As a data analyst, you might want to explore this relationship further and consider it in your churn prediction models.

### Content Type with Churn

![output_66_0](https://github.com/user-attachments/assets/b2337d64-da14-4e29-9bcd-84ac658fe561)
    
- **Churn and Content type**:
    - Movie content have the lowest churn rate followed by Tv shows and both.
    - User who have subscribe both have the high churn rate.

### Churn by Genre


![output_69_0](https://github.com/user-attachments/assets/c1556cc5-d7e4-47bb-9d36-acb4950b99e9)
    

- **Churn and Genre**:
    - Comedy have the high churn rate followed by the SCI-Fi, drama, fantasy and action have the lowest churn rate
    - Most users preferred the comedy genere followed by fantasy, drama,action and SCi-fi.

### Churn by Parental Control and Subtitle Enables


![output_72_0](https://github.com/user-attachments/assets/49a1c974-2fee-4b66-a513-a294bd518973)
    

- High churn rate in No parental control and no subtitle enabled.
- There is high number of users which have parent control and subtitle enabled. 

### Correlation with Churn

![output_75_0](https://github.com/user-attachments/assets/c07f9147-170b-4a3b-8975-af7e28879a9f)

1. Churn has a **negative correlation** with the following features:
   - `AccountAge`
   - `Viewinghoursperweek`
   - `Averageviewduration`
   - `Contentdownloadpermonth`
   
   This implies that as these features increase, churn tends to **decrease**.

2. On the other hand, churn has a **positive correlation** with the following features:
   - `Supportticketpermonth`
   - `userrating`
   - `watchlistsize`
   
   This suggests that as these features increase, churn tends to **increase**.

## Conclusion



1. **Paperless Billing**:
   - Customers who are not on paperless billing tend to have lower churn rates (correlation of approximately -0.98).
   - However, customers on paperless billing still exhibit a slightly higher churn rate (correlation of around -0.91).
   - **Insight**: Paperless billing significantly impacts churn behavior, and customers who prefer paperless billing are more likely to churn.

2. **Content Type**:
   - Movie content has the lowest churn rate, followed by TV shows and both.
   - Users who subscribe to both movie and TV show content have a higher churn rate.
   - **Insight**: Consider tailoring content recommendations based on user preferences to reduce churn.

3. **Genre Preferences**:
   - Comedy content has the highest churn rate, while genres like Sci-Fi, drama, fantasy, and action have lower churn rates.
   - Most users prefer comedy, followed by fantasy, drama, action, and Sci-Fi.
   - **Insight**: Personalizing content offerings based on genre preferences can improve retention.

4. **Parental Control and Subtitles**:
   - High churn occurs among users with no parental control and no subtitle enabled.
   - Many users have both parental control and subtitles enabled.
   - **Insight**: Enhancing parental control features and ensuring subtitle availability may positively impact retention.

5. **Correlations**:
   - Negative correlations:
     - AccountAge, Viewinghoursperweek, Averageviewduration, and Contentdownloadpermonth are associated with lower churn rates.
   - Positive correlations:
     - Supportticketpermonth, userrating, and watchlistsize are associated with higher churn rates.
   - **Insight**: These correlations can guide targeted strategies to reduce churn (e.g., improving customer support or enhancing content recommendations).

# Pipeline of Churn Predicting Machine learning Model

![Screenshot 2024-07-18 212935](https://github.com/user-attachments/assets/43022410-4cef-407c-ad23-37a3ed3293a7)
