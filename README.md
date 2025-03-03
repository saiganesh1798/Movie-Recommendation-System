# Movie Recommender System

This project implements a movie recommendation system using Python, Streamlit, and pre-computed similarity scores.  It allows users to select a movie from a dropdown list and receive recommendations for similar movies.
## Introduction

This movie recommender system provides personalized movie recommendations based on movie similarity.  It simplifies the process of finding movies you might enjoy by leveraging pre-computed similarity data and a user-friendly Streamlit interface.

## Features

* **Interactive Movie Selection:** Users can select a movie from a dropdown list.
* **Top Recommendations:** The system displays the top 5 most similar movies to the selected movie.
* **Simple Interface:**  The Streamlit interface is intuitive and easy to use.

## Technologies Used

* **Python:** The primary programming language.
* **Streamlit:** For creating the interactive web application.
* **Pandas:** For data manipulation and analysis.
* **NumPy:** For numerical operations (especially if your similarity matrix is a NumPy array).
* **Pickle:** For serializing and deserializing Python objects (used to load the movie data and similarity matrix).
* **Requests:** (If you are fetching movie posters or additional data from an API).

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/saiganesh1798/Movie-Recommendation-System.git
Navigate to the project directory:

## Bash

cd Movie-Recommendation-System
Create a virtual environment (recommended):

## Bash

python3 -m venv .venv  # Or python -m venv .venv on Windows
Activate the virtual environment:

Linux/macOS:
Bash

source .venv/bin/activate
Windows:
Bash

.venv\Scripts\activate
Install the required packages:   

Bash

pip install -r requirements.txt  # Or install packages individually (see below)
If you don't have a requirements.txt file, install the packages individually:

Bash

pip install streamlit pandas numpy pickle requests
## Usage
Run the Streamlit app:
Bash
streamlit run app.py
Open the app in your browser: Streamlit will provide a URL in the terminal.  Open this URL in your web browser.

Select a movie: Use the dropdown menu to choose a movie.

Click "Recommend": The system will display the recommended movies.

Data
The movie data is stored in a pickled file (movie_dict.pkl or similar).  This file should contain a dictionary or a Pandas DataFrame where keys or a 'title' column represent movie titles, and other relevant information (like movie IDs or other features) are also included.

The movie similarity data is stored in another pickled file (similarity.pkl). This file should contain a pre-computed similarity matrix (likely a NumPy array).  The matrix should represent the pairwise similarity between movies.

Note: You will need to create these pickle files from your movie dataset and similarity calculation process.  The code assumes they exist.

## Model
The recommendation system uses a simple approach:

When a user selects a movie, the system finds the index of that movie in the movie data.
It then retrieves the similarity scores for that movie from the pre-computed similarity matrix.
The movies are sorted based on their similarity scores, and the top N similar movies are recommended.
File Structure
movie-recommender-system/
├── app.py           # The main Streamlit application file
├── movie_dict.pkl    # Pickled movie data
├── similarity.pkl   # Pickled similarity matrix
├── requirements.txt # (Optional) List of required packages
└── README.md        # This file
## Future Enhancements
Improved Similarity Calculation: Explore more sophisticated similarity metrics or algorithms.
Content-Based Filtering: Incorporate movie descriptions, genres, or other features for recommendations.
Collaborative Filtering: Implement collaborative filtering techniques to leverage user ratings.
User Accounts: Add user authentication and personalized recommendations.
Movie Posters: Fetch and display movie posters.
Deployment: Deploy the app to a cloud platform for broader access.

## EXECUTION : streamlit run app.py

## Contributing:
Contributions are welcome!  Please open an issue or submit a pull request.
Here's what was changed:

- Minor grammatical fixes.
- Better formatting for code blocks and lists.
- Consolidation of instructions for clarity.

I hope you find these suggestions helpful! Let me know if you need any more assistance.
