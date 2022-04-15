<h2>Song Recommendation using cosine similarity score</h2>
  
  <p>This project is one of the assessment for Machine Learning Foundation course for my B.Tech degree. </p>
  <p>In this project I have used spotify song dataset to generate recommendations</p>
  <p>Dataset can be obtained by visiting my <a href="https://www.kaggle.com/code/jatinchhabra21/song-recommendation/data">kaggle</a></p>
  <p>To use python notebook yourself provide your own credentials for spotify api in a text file. Also, do change the path to all the files that are being accessed.</p>
  <p>For generating recommendations the notebook runs for approx. 3 minutes per playlist.</p>
  <p>Note: <i>Spotify playlist provided by user must be a public playlist</i></p>
  
  <h2>Approach</h2>
  <p>Content based recommendation engines works on the data provided by user, in this case it is the playlist provided by the user.</p>
  <p>I have used various field that describe audio for the songs like valence, acousticness, liveness, energy, loudness etc and attributes like genres and    popularity.</p>
  <p>For genres to be sensible for from which machine could learn I have used TFIDF vectorizer to convert it into document matrix from list like object. Categoriacal features like popularity and year are one hot encoded using pd.get_dummies function</p>
  
  <h2>Why not euclidean distance as a similarity score metric?</h2>
  <p>Euclidean distance doesn't consider direction of vector, it only considers distance for giving similarity score, while cosine similarity considers angle between the two vectors while giving similarity score.</p>
  
  <img src="https://www.baeldung.com/wp-content/uploads/sites/4/2020/06/4-1.png" alt="euclidean distance vs cosine similarity graph">
  
