
## Recommendation Systems

Data: https://www.kaggle.com/datasets/rxsraghavagrawal/book-recommender-system

Reference: https://www.analyticsvidhya.com/blog/2021/06/build-book-recommendation-system-unsupervised-learning-project/

Recommedations can be based on three types

- **Content Based Filtering:** Under this type of recommendations, tags are used. For example if user 1 reads Book A, B with certain tags associated with them and there are other books C, D which have similar tags associated to them then user 1 will be recommended books C and D.


- **Collaborative Based Filtering:** This type of recommendation is based on users. If two users are watching similar contents then their respective choices will be recommended to each other as well. For example, if user 1 reads Books A, B and user 2 reads Books B, C then user 1 would be recommended Book C while user 2 will be recommended Book A.


- **Hybrid Filtering**: This is a mixture of both above methods.

For the scope of this project, we would be implementing **Collorative Based Filtering**. This used matrix factorization, for which we will be using pivot of our data as below.

#### Pre-processing and Implementation

As part of pre-processing, encoded characters are replaced with ascii characters. All the titles of the data are converted to lower case as finally we will be taking user input to recommend books.

To implement collaborative based filtering, here we are using matrix factorization to train our KNN model. This matris is based on different users and the ratings they gave to books. We will only be considering books with atleast 25 reviews and only users who have rated atleast 100 books would be considered for total review count.

The matrix formed is huge with multiple zero values, hence we would be converting it to sparse matrix for our use.

Finally using the above dataset, a recommendation model is created using KNN algorithm.
