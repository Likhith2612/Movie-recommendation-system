**Movie Recommendation System**
Based on Netfilx dataset (from Kaggle)

1. **Importing Dataset:**
   - Reads the Netflix dataset from a CSV file into a Pandas DataFrame.

2. **Data Preprocessing:**
   - Rearranges columns for better readability.
   - Drops rows with missing values in the 'description' column.
   - Fills any remaining missing values in the 'description' column with an empty string.

3. **Input and Output Setup:**
   - Defines the input features (`x`) as the first four columns and the output (`y`) as the last two columns.

4. **Train-Test Split:**
   - Splits the data into training and testing sets using the `train_test_split` function from `sklearn.model_selection`.

5. **Text Vectorization:**
   - Utilizes TF-IDF vectorization on movie descriptions using `TfidfVectorizer` from `sklearn.feature_extraction.text`.

6. **Cosine Similarity Calculation:**
   - Calculates the cosine similarity between movies based on their descriptions using `linear_kernel` from `sklearn.metrics.pairwise`.

7. **User Input:**
   - Takes user preferences for country, genre, and movie duration.

8. **Recommendation System:**
   - Filters the dataset based on user preferences.
   - If no exact matches are found, it recommends similar movies based on genre using cosine similarity.
   - Outputs recommended movies along with brief descriptions.
9. **Predication example:**

10. Enter your preferred country: India
Enter your preferred movie genre: TV shows
Enter your preferred movie duration: seasons
Enter your preferred release year: 2021
Recommended movies for Kota Factory:
- Little Things
- Hometown Cha-Cha-Cha
- I Need Romance
- Feels Like Ishq
- Generation 56k
- Let's Eat
- Mad for Each Other
- Use For My Talent
- Club Friday The Series 8
- Beauty and the Bitches
Recommended movies for The Big Day:
- Too Hot To Handle: Latino
- Too Hot to Handle: Brazil
- Too Hot to Handle
- The Wedding Coach
- Marriage or Mortgage
- Motel Makeover
- The Parisian Agency: Exclusive Properties
- Don't be the First one
- Ainori Love Wagon: Asian Journey
- Blown Away
