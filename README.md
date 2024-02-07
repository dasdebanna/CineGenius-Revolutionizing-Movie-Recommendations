
![Logo](https://github.com/dasdebanna/CineGenius-Revolutionizing-Movie-Recommendations/blob/main/images/movie-recommendation.png)


# CineGenius: Revolutionizing Movie Recommendations

CineGenius is a Python-powered Movie Recommendation System, blending Data Science and Machine Learning for personalized movie suggestions. It's more than a project; it's an immersive journey where Python skills meet real-world application. Dive into data manipulation, algorithmic modeling, and refine your recommendations. CineGenius isn't just about movies; it's about honing your Python, Data Science, and Machine Learning expertise while crafting bespoke cinematic experiences.


## Dataset Used
I have used the TMDB 5000 Movie Dataset. That data I have used consists of 5000 credits in the ```tmdb_5000_credits.csv``` file, applied over 5000 movies in the ```tmdb_5000_movies.csv```.


## Essential Libraries
```nltk```, ```scikit-learn```, ```NumPy``` and ```Pandas```.
## Data Pre-processing
Data pre-processing is a crucial step in any machine learning project. It involves cleaning and transforming raw data into a format that is suitable for analysis and modeling. Below are the data pre-processing steps applied to ```CineGenius: Revolutionizing Movie Recommendations```

```Dataset Description:```

The dataset consists of information about movies, including their titles, overviews, genres, keywords, cast, crew, and other relevant details.

```Data Pre-processing Steps:```

1.```Loading the Data:```

The dataset is loaded using the pandas library, which provides functionalities for data manipulation and analysis in Python.

2.```Handling Missing Values:```

Any rows with missing values are removed using the dropna() function to ensure data integrity.

3.```Parsing JSON Columns:```

Columns containing JSON data, such as genres, keywords, cast, and crew, are parsed using the ast.literal_eval() function to convert them into Python objects.

4.```Extracting Relevant Information:```

For JSON columns, only relevant information (e.g., names of genres, keywords, cast members) is extracted and retained for further analysis.

5.```Limiting Cast Members:```

Only the first three cast members are retained for simplicity. This is achieved by slicing the cast list.

6.```Extracting Director Information:```

From the crew column, the names of directors are extracted based on their job title.

7.```Text Processing:```

Text data, such as overviews, is processed by splitting it into individual words for further analysis.

8.```Combining Features:```

Relevant features (overviews, genres, keywords, cast, crew) are combined to form a consolidated set of tags representing each movie.

9.```Vectorization:```

The tags are then vectorized using the CountVectorizer from scikit-learn, which converts text data into numerical vectors suitable for machine learning algorithms.

10.```Cosine Similarity Calculation:```

Cosine similarity is calculated between the vectors of movie tags to measure the similarity between movies.

11.```Recommendation Function:```

A function is created to recommend similar movies based on the cosine similarity scores.

12.```Saving Processed Data:```

Finally, the pre-processed data and similarity scores are saved using the pickle library for future use.
## Model Building
Model building is a crucial phase in machine learning projects where we use pre-processed data to train a model that can make predictions or recommendations based on input data. Below are the model building steps applied to ```CineGenius: Revolutionizing Movie Recommendations```

```Model Description:```

The model utilizes cosine similarity to recommend movies similar to a given input movie. Cosine similarity measures the cosine of the angle between two non-zero vectors and is commonly used to determine similarity between documents or in this case, movies.

```Model Building Steps:```

1.```Loading Pre-processed Data:```

The pre-processed movie dataset and cosine similarity scores are loaded from the saved pickle files using the pickle library.

2.```Defining the Recommendation Function:```

A function named recommend() is defined to recommend similar movies based on the input movie title.
Inside the function, the index of the input movie in the dataset is retrieved.
The cosine similarity scores between the input movie and all other movies are sorted in descending order.
The titles of the top similar movies (excluding the input movie itself) are printed as recommendations.

3.```Model Evaluation:```

Since this is a recommendation system, there is no traditional model evaluation. Instead, recommendations are visually inspected and assessed for relevance and coherence.

4.```Recommendation Function Usage:```

The recommend() function is called with a sample input movie title to demonstrate its functionality.
The function outputs a list of recommended movies based on the cosine similarity scores.
## Screenshots

![App Screenshot](https://drive.google.com/file/d/1h-0ywmnKiGQtFoy21eniNb0L_sNqn4n6/view?usp=drive_link)


## Conclusion
Our movie recommendation system, powered by cosine similarity, revolutionizes the way users discover films. By intelligently analyzing pre-processed data, we deliver tailored recommendations that captivate and inspire. Seamlessly blending advanced techniques, our system opens doors to new cinematic adventures, enriching user experiences with every suggestion. As we continue to innovate, the future holds boundless opportunities for even more personalized and engaging recommendations, propelling us into a realm of endless cinematic exploration and enjoyment.
## Feedback

If you have any feedback, please reach out to me at contact@dasdebanna.tech

