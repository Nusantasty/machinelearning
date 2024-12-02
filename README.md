# Nusantasty: Machine Learning for Recipe Recommendations

This repository hosts the code and resources for a machine learning project designed to recommend recipes based on ingredients provided by users.

## Project Structure

- `data/`: Includes datasets used for training and evaluation.
- `notebooks/`: Contains Jupyter notebooks for exploratory data analysis and model development.
- `.gitignore`: Specifies files and directories to exclude from version control.

## Getting Started

### Prerequisites

- Python 3.10+
- Jupyter Notebook
- Install dependencies listed in `requirements.txt`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/rajabagung/Nusantasty-ML-Part.git
   cd Nusantasty-ML-Part
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

- Open the notebooks in the notebooks/ directory to explore datasets and train models.
- Modify and execute the notebooks to generate recipe recommendations based on your input data.
- 
## Datasets

- `recipes.csv`: Contains recipe information including ingredients, instructions, and nutritional data.
- `ratings.csv`: Contains user ratings for various recipes.

### Recommended for You

Uses K-Nearest Neighbors (KNN) for collaborative filtering to suggest recipes based on user preferences.

1. User Interactions:

- Users choose disliked ingredients and allergies, which are stored in Firebase.
- Users rate recipes, and these ratings are also stored in Firebase.

2. Collaborative Filtering:

- Calculate the similarity between the data points (recipes) and all training data.
- Recommend recipes with the highest similarity while considering the user's dislikes and preferences.

<br>

### Get Recipes

Applies TF-IDF vectorization and cosine similarity to recommend recipes based on the ingredients users have at home.

1. User Inputs:

- Users choose disliked ingredients and allergies, which are stored in Firebase.
- Users input ingredients they have and request recipe generation.

2. Content-Based Filtering:

- Retrieve stored dislikes and allergies from Firebase.
- Apply TF-IDF vectorization on user input ingredients.
- Compute cosine similarity to find top-N similar recipes.
- Generate and recommend recipes that avoid disliked or allergenic ingredients.

## License

© 2024
