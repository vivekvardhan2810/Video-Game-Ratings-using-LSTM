# Video-Game-Ratings-using-LSTM
This repository contains a project that uses a Long Short-Term Memory (LSTM) neural network to predict video game ratings based on various features such as title, genre, platform, release year, and number of players.

# Dataset

<p>The dataset is taken from kaggle (https://www.kaggle.com/datasets/dem0nking/video-game-ratings-dataset/data) :</p>

<b>Title:</b> The name of the video game.

<b>Genre:</b> The genre of the video game.

<b>Platform:</b> The platform(s) on which the game is available.

<b>ReleaseYear:</b> The year the game was released.

<b>NumPlayers:</b> The number of players supported.

<b>AvgRating:</b> The average rating of the game.

# Project Structure

<b>Data Preprocessing</b>

<ul>
  <li><b>Encoding Categorical Variables:</b> Convert Title, Genre, and Platform to numerical values using LabelEncoder.</li>
  <li><b>Normalizing Numerical Variables:</b> Scale ReleaseYear and NumPlayers to a range of 0 to 1 using MinMaxScaler.</li>
  <li><b>Feature and Label Preparation:</b> Separate features (X) and the target variable (y).</li>
  <li><b>Data Splitting:</b> Split the dataset into training and testing sets (80-20 split).</li>
</ul>

Building the LSTM Model
Model Definition: Create a sequential LSTM model with:
Two LSTM layers with 50 units each and dropout for regularization.
Dense layers for output.
Model Compilation: Use 'adam' optimizer and 'mean_squared_error' loss function.
Data Reshaping: Reshape input data to fit LSTM input requirements.

Training the Model
Train the model on the training data for 10 epochs with a batch size of 1.

Evaluating the Model
Loss Evaluation: Calculate the test loss.
Predictions: Generate predictions on the test set.

Calculating Metrics
Mean Absolute Error (MAE): Measure the average magnitude of errors.
Custom Accuracy: Define accuracy based on predictions within a specified threshold (±0.5).
