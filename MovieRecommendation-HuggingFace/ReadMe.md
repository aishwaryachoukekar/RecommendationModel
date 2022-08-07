## Movie Recommendation Model using Text Similarity of Hugging Face

Data Source: https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?resource=download
(only movies_metadata.csv file is used from this link)

### Assumption:
  - This model will focus on recommendations based on similar genres and similarity in discription of movies.
  - Only unique movie titles will be considered

### Data pre-processing
  - Pre-processing file is separately attached to clean dataset and make it more usable for model training.
  - Cleaned dataset is exported as movies.csv which is then uploaded for final model

### Model

#### Libraries used
  - Hugging Face (sentence-transformers)
  - Regex

#### Ideology
  - Model will recommend movies based on **genres** and **movie description**.
  - Weighted score is considered of these two to assign to movies in database.
  - Based on input movie name, bunch of similar movies is filtered based on similar genres. Each movie can have more than one genre. Count of similar genres is given weight of **60%** and the similarity score calculated for input movie description and filtered movies is given a weight of **40%**.
  - This final score is then ordered in descending order.
  - Top 10 movies based on these scores are then displayed as recommendations.
