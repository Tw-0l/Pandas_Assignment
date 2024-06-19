# Instagram User Dataset Analysis

This project focuses on analyzing the `instagram_users.csv` dataset, which contains various attributes related to Instagram users. The dataset has 65,326 rows and 18 columns, with no missing values. The columns represent different features of user profiles, such as the number of posts, followers, following, and engagement metrics. The goal is to process and analyze the data to gain insights into the characteristics of real and fake Instagram accounts.

### Dataset Overview
- **Number of rows:** 65,326
- **Number of columns:** 18
- **Size of dataset:** 1,175,868 entries
- **Data Types:** 
  - `int64`: 7 columns
  - `float64`: 10 columns
  - `object`: 1 column (class)

### Columns and Descriptions
1. **pos**: Number of total posts that the user has ever posted
2. **flg**: Number of following
3. **flr**: Number of followers
4. **bl**: Length (number of characters) of the user's biography
5. **pic**: Profile picture availability (0 if no profile picture, 1 if has)
6. **lin**: External URL availability (0 if no external URL, 1 if has)
7. **cl**: Average number of characters of captions in media
8. **cz**: Percentage of captions that have almost zero (<=3) length
9. **ni**: Percentage of non-image media
10. **erl**: Engagement rate (ER) for likes
11. **erc**: Engagement rate for comments
12. **lt**: Percentage of posts tagged with location
13. **hc**: Average number of hashtags used in a post
14. **pr**: Average use of promotional keywords in hashtags
15. **fo**: Average use of follower hunter keywords in hashtags
16. **cs**: Average cosine similarity between all pairs of posts a user has
17. **pi**: Average interval between posts (in hours)
18. **class**: User type (r for real/authentic user, f for fake user/bought followers)

### Key Analysis Steps
1. **Reading and Initial Inspection:**
   - Imported the dataset using `pandas`.
   - Inspected the number of rows and columns.
   - Checked for the presence of null values.

2. **Data Cleansing:**
   - Removed duplicate rows, reducing the dataset to 64,244 rows.

3. **Column Renaming:**
   - Renamed columns for better clarity.
   - Updated the 'class' column to more descriptive labels ('fake' and 'real').

4. **Descriptive Statistics:**
   - Generated summary statistics for all columns, including count, mean, standard deviation, min, max, and quartiles.
   
5. **Data Exploration:**
   - Printed the first and last five rows of the dataset.
   - Counted the number of real and fake accounts.
   
### Summary Statistics
- **Num_posts:** Mean = 179.55, Std = 729.17, Min = 0, Max = 76,200
- **Num_following:** Mean = 1,202.47, Std = 21,889.54, Min = 0, Max = 3,900,000
- **Num_followers:** Mean = 2,297.04, Std = 2,572.94, Min = 0, Max = 8,800
- **Biography_length:** Mean = 58.46, Std = 64.23, Min = 0, Max = 555
- **Picture_availability:** Mean = 0.96, Std = 0.20, Min = 0, Max = 1
- **Link_availability:** Mean = 0.29, Std = 0.45, Min = 0, Max = 1
- **Average_caption_length:** Mean = 138.82, Std = 216.79, Min = -1, Max = 3,644
- **Caption_zero:** Mean = 0.25, Std = 0.34, Min = 0, Max = 1
- **Non_image_percentage:** Mean = 0.20, Std = 0.25, Min = 0, Max = 1
- **Engagement_rate_like:** Mean = 19.47, Std = 122.04, Min = 0, Max = 26,650
- **Engagement_rate_comment:** Mean = 1.16, Std = 5.86, Min = 0, Max = 1,009.09
- **Location_tag_percentage:** Mean = 0.21, Std = 0.30, Min = 0, Max = 1
- **Average_hashtag_count:** Mean = 0.52, Std = 1.16, Min = 0, Max = 54
- **Promotional_keywords:** Mean = 0.03, Std = 0.22, Min = 0, Max = 10
- **Followers_keywords:** Mean = 0.05, Std = 0.52, Min = 0, Max = 40
- **Cosine_similarity:** Mean = 0.02, Std = 0.10, Min = -1, Max = 1
- **Post_interval:** Mean = 22.44, Std = 74.39, Min = 0, Max = 11,904

### Real vs Fake Accounts
- **Real accounts:** 32,460
- **Fake accounts:** 31,784

### Insights
- Real accounts tend to have fewer posts and followers than fake accounts.
- Fake accounts often exhibit higher engagement rates, possibly due to bought followers.
- Real accounts have more complete profiles, with profile pictures and bios.
- Fake accounts may use promotional keywords and follower hunter keywords more frequently.

This analysis provides a comprehensive overview of the dataset, highlighting key differences between real and fake Instagram accounts. The processed data can be used for further analysis and modeling, such as training a machine learning model to classify real and fake accounts.
