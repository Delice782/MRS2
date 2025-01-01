# Movie Recommendation System
This project aims to build a content-based movie recommendation system using a dataset that combines information from Netflix, Rotten Tomatoes, Metacritic, and IMDb. The recommendation system suggests movies based on their descriptions and other features using techniques like TF-IDF vectorization and cosine similarity.

## Getting Started
Follow these instructions to get a copy of the project up and running on your local machine for testing purposes.

### Prerequisites
- Python 3.x
- Jupyter Notebook
- Libraries: numpy, pandas, scikit-learn, seaborn, matplotlib, nltk, plotly, wordcloud, joblib, streamlit

### Installing Dependencies
Use the following commands to install the required libraries:
```sh
pip install numpy pandas scikit-learn seaborn matplotlib nltk plotly wordcloud joblib
```

### Project Files
- `Final Project Movie Recommendation System.ipynb`: Jupyter Notebook containing the code for data preprocessing, exploration, model building, evaluation, and recommendations.
- `Movie_data.csv`: Cleaned dataset saved after preprocessing.
- `content_based_recommender.pkl`: Pickle file containing the trained TF-IDF vectorizer, cosine similarity matrix, and movie indices mapping.
- `Merged_data.pkl`: Pickle file containing the cleaned and preprocessed movie data.

## Project Workflow
1. **Import Libraries**: Import necessary libraries for data processing, visualization, and modeling.

2. **Load and Preprocess Data**: 
   - Load the dataset.
   - Remove duplicates.
   - Drop columns with more than 30% missing data.
   - Impute missing values using appropriate strategies.

3. **Exploratory Data Analysis (EDA)**:
   - Generate descriptive statistics.
   - Visualize data distributions and correlations.
   - Analyze genre distribution and rating trends over the years.

4. **Feature Engineering**:
   - Clean and preprocess text data.
   - Apply TF-IDF vectorization to movie descriptions.
   - Calculate cosine similarity between movie vectors.

5. **Building the Recommendation System**:
   - Create functions to get movie indices and recommend similar movies.
   - Evaluate the recommendation system with different movie titles.

6. **Model Deployment**:
   - Save the trained model components using joblib.
   - Load the model components for making recommendations.

## Running the Notebook
1. Open the `Final Project Movie Recommendation System.ipynb` notebook in Jupyter.
2. Execute the cells sequentially to preprocess data, perform EDA, build and evaluate the recommendation system, and save the model.
3. Test the recommendation system with sample movie titles to see the results.

## Hosting with Streamlit
To host our application using Streamlit:
1. Navigate to the project directory:
    ```
    cd path/to/your/project
    ```
2. Run the Streamlit application:
    ```
    streamlit run app.py
    ```
3. Open the provided local URL in your browser to interact with the recommendation system.

## Functions
### Data Preprocessing
- `xStem(text)`: Apply stemming to text data.
- `get_movie_title_index(movie, indices)`: Get the index of a movie based on its title.
- `recommend_movie_titles(movie_title, indices, cosine_similarity)`: Recommend similar movies based on the input title.

### Visualization
- `display_movie_recommendations(selected_movie, movie_titles, poster_urls)`: Display recommended movie titles and their posters.

### Model Deployment
- `get_poster_url(poster_path)`: Get the poster URL for a recommended movie.
- `recommend_movies_and_posters(input_movie_title)`: Recommend movies and fetch their posters based on a given movie.
- `recommend_movies_loaded_model(title, loaded_cosine_sim)`: Use the loaded model for recommendations.

## Testing
Test the recommendation system with sample movie titles such as "The Avengers", "The Butterfly's Dream", "I Am Mother", "Hedgehogs", "2067", and "Let's Fight Ghost" to evaluate its performance.

## Video Demonstration
[The link to our video testing our model]  (https://youtu.be/XKgmr27-TXU?si=ug3Yln5UmkNPBUgE)



