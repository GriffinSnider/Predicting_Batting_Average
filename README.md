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
       ![image](https://github.com/user-attachments/assets/42843a89-9f53-4655-9620-0a240bb27cd7)
      - Heatmap of Batting Stats:
       ![image](https://github.com/user-attachments/assets/350e39e8-08ea-4a12-833c-04eef57725b4)
      - Batting Stats Compared to Batting Average:
       ![image](https://github.com/user-attachments/assets/92a17480-727f-49df-afaf-1022a97c1aa9)
      - Batting Average by Batting Hand & Throwing Hand:
       ![image](https://github.com/user-attachments/assets/f9fb698e-7775-4ce7-9e40-900561687113)

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
         -![image](https://github.com/user-attachments/assets/b013cbf8-d311-4bca-b47a-b535af4ef8e5) 
           ![image](https://github.com/user-attachments/assets/63f354f9-0bfb-4ba1-ad07-b5dbaac480f8)
           ![image](https://github.com/user-attachments/assets/0809da7e-8ea7-463e-a1b7-569331fce028)
   - Random Forest Regressor:
           ![image](https://github.com/user-attachments/assets/99474559-7d2b-4169-8c08-f7e54d839a76)
           ![image](https://github.com/user-attachments/assets/cd23e1f9-3c6a-4b0c-9aec-b95c281585ee)
           ![image](https://github.com/user-attachments/assets/5a0542f0-d0e2-4f42-8936-8a05dfa702bd)
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

