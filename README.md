# Prediciting Baseball Batting Average
Use player statistics to predict batting average and find influences that affect hitting performance.
## Project Overview
The dataset comes from [Sean Lahman’s Baseball Database](http://seanlahman.com/), which contains statistics on batting, pitching, fielding, standings, team stats, managerial records, postseason data, and more, dating back to 1871. My focus is on batting data, analyzing how different stats contribute to a player's batting average. By using this data, regression machine learning techniques can be applied to predict batting performance. These predictions can help baseball analysts better understand player performance trends.
## Project Workflow
1. **Data Cleaning & Preprocessing**
   - Remove/fill in unneeded or missing data
   - Filtering out players with few at-bats
2. **Exploratory Data Analysis**
   - Look for patterns in the data to see what stats impact batting average
   - Made charts and graphs to get a better idea of trends in player performance
      - Visualizion distrubution of six batting statistics:
       ![image](https://github.com/user-attachments/assets/6410bbbe-a452-4986-bf4b-b066c3e3871d)
      - Heatmap of Batting Stats:
       ![image](https://github.com/user-attachments/assets/f230d7bb-09cb-4dca-bf85-b273dbfd28c7)
      - Batting Stats Compared to Batting Average:
       ![image](https://github.com/user-attachments/assets/db5ce619-a608-4ce1-8af5-6be96892f762)
      - Batting Average by Batting Hand & Throwing Hand:
       ![image](https://github.com/user-attachments/assets/8d810bce-f9f0-4d25-b0b1-e30c3c03a75b)

3. **Splitting The Data Into Training**
   - Separated the data so the model could learn from some players while being tested on others
   - Used a 70/15/15 split to balance training, validation, and testing
4. **Feature Engineering**
   - Created new features from existing stats to try to improve model predictions.
5. **Rescaling the data**
   - Used StandardScaler to standardize features by removing the mean and scaling to unit variance
6. **Train/Tune Models**
   - K-Nearest Neighbors:
   - . 
         -![image](https://github.com/user-attachments/assets/56d4cda7-3cf8-43c7-91bf-8ba5283bf107)
           ![image](https://github.com/user-attachments/assets/588649bf-65b0-4b83-9699-16d63e241b00)
           ![image](https://github.com/user-attachments/assets/95827d0e-ae15-44f6-82b0-4322ac4af86d)
   - Random Forest Regressor:
           ![image](https://github.com/user-attachments/assets/dc7307ff-352d-44eb-b694-cd370f6daf48)
           ![image](https://github.com/user-attachments/assets/5db3002b-573f-417a-9be9-9c2bc7291b24)
           ![image](https://github.com/user-attachments/assets/919d441b-3cbe-4a9f-92bf-c630aa7606c5)
   - Evaluated performance using:
     - Mean squared error (MSE)
     - R2 score
     - Cross-validation
7. **Overall**
   - Both KNN and Random Forest models capture key patterns in the data, but the Random Forest model provided a better result
   - Baseball average is inherently difficult to predict due to its dependence on external and situational factors such as pitcher matchups, ballpark effects, injuries, and changes in player performance throughout the season
   - While the dataset included many offensive statistics, batting average is influenced by several other factors that are missing from this dataset. Some of the features that could of have been beneficial:
       - Pitching related features
          -ERA, WHIP, strikeout rate, pitchers throwing hand, pitch type data
       - Situational factors
          - Ballpark factors, weather conditions, home vs. away splits
          - Game situation data (scoring positon, late-game, clutch at bats)
       - Fatigue or injuries
          - Days of rest between games, injury history
       - More advanced statistics
          -WAR, xBA, wOBA, BABIP, OBP, SLG, OPS, XBH. NP, etc.

