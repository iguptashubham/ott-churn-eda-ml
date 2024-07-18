# Streaming OTT  Subscription

For this analysis, we'll be examining customer churn data from a leading subscription-based streaming service. This industry giant boasts a vast library of movies, TV shows, and original content. Understanding why customers discontinue their subscriptions will be crucial in optimizing the user experience, reducing churn, and maximizing customer lifetime value.

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


```python
uni_plot(df,'MonthlyCharges', h_bins=30,h_hue='Churn')
```


    
![png](output_36_0.png)
    


1. **Churn and Monthly Charges:**
   - Churn rates tend to increase as monthly charges increase. Users with higher monthly charges are more likely to churn.
   - Low churn occurs when monthly charges are low.

2. **Subscription Distribution:**
   - There's a relatively high number of low monthly subscriptions, gradually decreasing toward higher subscription tiers.

3. **Monthly Charge Statistics:**
   - Minimum monthly price: 4.99
   - Maximum monthly price: 19.99

### Viewing Hours Per Week


```python
uni_plot(df,'ViewingHoursPerWeek', h_bins=30, h_hue='Churn')
```


    
![png](output_39_0.png)
    


1. **Churn and Viewing Hours:**
   - Users with higher weekly viewing hours are less likely to churn compared to those with lower viewing hours.
   - High churn occurs among users who view less than or equal to four hours.
   - Users with viewing hours between 30 and 40 exhibit relatively stable churn.

2. **Viewing Hours Statistics:**
   - Average weekly view hours: 20.5
   - Minimum weekly view hours: 1
   - Maximum weekly view hours: 40

### Average Viewing Duration


```python
uni_plot(df, 'AverageViewingDuration', h_bins=30, h_hue='Churn')
```


    
![png](output_42_0.png)
    


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


```python
uni_plot(df, 'ContentDownloadsPerMonth', h_hue='Churn', h_bins=30)
```


    
![png](output_45_0.png)
    


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


```python
uni_plot(df, 'UserRating', h_bins=30, h_hue='Churn')
```


    
![png](output_48_0.png)
    


1. **Churn and User Rating:**
   
   - There is no relationship between rating and churn because rating 1 to 5 there is relatively stable churn.
   - OTT streaming get relatively equal ratings.
    
2. **User Rating Statistics :**

   - Minimum is 1.
   - Maximum is 4.99
   - Average is 3.002.

### Support Ticket Per month


```python
uni_plot(df,'SupportTicketsPerMonth', h_bins=15,h_hue='Churn')
```


    
![png](output_51_0.png)
    


1. **Churn and Support Ticket:**
   
   - From the illustration, it shows that the higher the ticket generate, the users most likely to churn
- there is significantly low churn rate when there is no ticket generated. but when the ticket generated it also increaes the churn rate. 
   - Most churn rate are when the ticket generated 6 to 8.
    
2. **Support Ticket Statistics :**

   - Minimum is 0.
   - Maximum is 9.99
   - Average is 4.5.002.

### Watch List Size


```python
uni_plot(df,'WatchlistSize',h_bins=25, h_hue='Churn')
```


    
![png](output_54_0.png)
    


1. **Churn and Watch List Size:**
   
   - There is no relationship between Watchlist and churn because there is relatively stable churn.
    
2. **User Rating Statistics :**

   - Minimum is 0.
   - Maximum is 24.99
   - Average is 12.02.

### Churn by Subscription


```python
subs_ = df.groupby(['SubscriptionType','Churn'], as_index=False).size()
subs1 = subs_[subs_['Churn']==0]
subs2 = subs_[subs_['Churn']==1]
plt.figure(figsize = (9,5))
ax = sns.barplot(data = subs1, x = 'SubscriptionType', y = 'size',errorbar=None, label = 'Not Churned', edgecolor = 'black')
ax1 = sns.barplot(data = subs2, x = 'SubscriptionType', y = 'size',errorbar=None,ax = ax, label = 'Churned',edgecolor = 'black')
ax1.axhline(subs2['size'].mean(), color = 'black', linestyle = '--', alpha = 0.5)
ax1.plot(0.478,18000,marker='^')
ax1.text(0.460,21000,'Average Churn', rotation = 'vertical', mouseover = True)
for i in ax1.containers:
    ax1.bar_label(i, label_type = 'center', color = 'white')
plt.title('Churn by Subcription')
plt.legend(loc='upper left', bbox_to_anchor=(1.0, 1.0), frameon=False)
plt.grid(True)
plt.show()
```


    
![png](output_57_0.png)
    


1. **Churn Rate by Subscription Type**:
   - The churn rate is highest among Basic subscribers, followed by Standard and Premium.
   - Specifically, users who subscribe to the Basic plan tend to have a higher churn rate.

2. **Premium Subscribers**:
   - Premium subscribers exhibit the lowest churn rate across all subscription types.
   - This suggests that Premium subscribers are more likely to stay with the service.

3. **User Preferences**:
   - Most users prefer the Premium subscription, followed by Standard and then Basic.


### Payment Method and Paperless Billing


```python
billing = df.groupby(['PaymentMethod','PaperlessBilling','Churn'], as_index=False).size()
billing = billing.pivot_table(index = 'PaymentMethod', columns = ['PaperlessBilling','Churn'], values='size')
```


```python
ax = billing.plot(kind='barh', stacked=True, figsize=(10, 5), width = 0.7, edgecolor = 'black')
ax.legend(loc='upper left', bbox_to_anchor=(1.0, 1.0), frameon=False)
for c in ax.containers:
    ax.bar_label(c, label_type='center', color = 'white')
plt.title('Churn By Payment Method and Paperless Billing')
plt.xlabel('')
plt.xticks([])
plt.grid(True)
plt.tight_layout()
plt.show()
```


    
![png](output_61_0.png)
    


1. **Churn and Payment Method:**
   
    - from this illustration, Users with electronic check have the higher churn rate followed by mail check  and bank transfer and credit.
    - Paperless billing affecting the churn rate is relatively very low.
3. **Overall Insights:**

    - users with Payment method which takes time and effort have thr highest churn rate as compared to the payment method that require less effort.


```python
plt.figure(figsize = (10,8))
sns.heatmap(billing.corr(), annot = True, linecolor='white', linewidths=3,cbar_kws={'orientation': 'horizontal'}, cmap="crest")
plt.title('Correlation between Paperless billing and Churn')
plt.show()
```


    
![png](output_63_0.png)
    


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


```python
content = df.groupby(['ContentType','Churn']).size().unstack()
ax = content.plot(kind = 'barh',stacked = True, width=0.65, figsize = (12,5),edgecolor = 'black')
for i in ax.containers:
    ax.bar_label(i, label_type = 'center', fontsize = 12, color = 'white')
ax.set_title('Churn by Content Type')
ax.legend(loc='upper left', bbox_to_anchor=(1.0, 1.0), frameon=False)
plt.show()
```


    
![png](output_66_0.png)
    


- **Churn and Content type**:
    - Movie content have the lowest churn rate followed by Tv shows and both.
    - User who have subscribe both have the high churn rate.

### Churn by Genre


```python
genre = df.groupby(['GenrePreference','Churn']
                  ).size().unstack().sort_values(by = 1.0, ascending = True)
#plot
ax = genre.plot(kind = 'barh', stacked = True, width = 0.85, figsize = (10,5),edgecolor = 'black')
for i in ax.containers:
    ax.bar_label(i, label_type = 'center', fontsize = 13, color = 'white')
plt.title('Churn by Genre')
ax.legend(loc='upper left', bbox_to_anchor=(1.0, 1.0), frameon=False)
plt.xticks([])
plt.show()
```


    
![png](output_69_0.png)
    


- **Churn and Genre**:
    - Comedy have the high churn rate followed by the SCI-Fi, drama, fantasy and action have the lowest churn rate
    - Most users preferred the comedy genere followed by fantasy, drama,action and SCi-fi.

### Churn by Parental Control and Subtitle Enables


```python
parent = df.groupby(['ParentalControl','Churn']).size().unstack()
subtitle = df.groupby(['SubtitlesEnabled','Churn']).size().unstack()

#plot
fig, ax = plt.subplots(1,2,figsize = (18,6))
#plot 1
parent.plot(kind = 'barh', stacked = True, edgecolor = 'black', ax = ax[0])
ax[0].set_title('Churn by Parent Control')
for i in ax[0].containers:
    ax[0].bar_label(i, label_type = 'center', color = 'white', fontsize = 13)
#plot2
subtitle.plot(kind = 'barh', stacked = True, edgecolor = 'black', ax = ax[1])
ax[1].set_title('Churn by Subtitle')
for i in ax[1].containers:
    ax[1].bar_label(i, label_type = 'center', color = 'white', fontsize = 13)
plt.show()
```


    
![png](output_72_0.png)
    


- High churn rate in No parental control and no subtitle enabled.
- There is high number of users which have parent control and subtitle enabled. 

### Correlation with Churn


```python
corr_ = df[['AccountAge', 'ViewingHoursPerWeek',
       'AverageViewingDuration', 'ContentDownloadsPerMonth', 'UserRating',
       'SupportTicketsPerMonth', 'WatchlistSize', 'Churn']].corr()
plt.figure(figsize = (18,8))
sns.heatmap(corr_, annot = True, cmap = 'RdBu', cbar = True, linecolor='black', linewidths=1.1)
plt.title('\n Coorelation \n', fontsize = 17)
#plt.tight_layout()
plt.show()
```


    
![png](output_75_0.png)
    


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

