# Movie Recommendation System

This repository contains a Python script for building a movie recommendation system using a dataset of movies' information. The recommendation system uses content-based filtering to suggest movies based on their genres, keywords, cast, crew, and overview.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
  - [Merging Data](#merging-data)
  - [Selecting Relevant Columns](#selecting-relevant-columns)
  - [Handling Missing Data](#handling-missing-data)
  - [Processing Genres, Keywords, Cast, and Crew](#processing-genres-keywords-cast-and-crew)
  - [Text Data Preprocessing](#text-data-preprocessing)
- [Feature Engineering](#feature-engineering)
  - [Creating Movie Tags](#creating-movie-tags)
  - [Dropping Unnecessary Columns](#dropping-unnecessary-columns)
  - [Text Stemming](#text-stemming)
  - [Vectorizing Text Data](#vectorizing-text-data)
- [Movie Recommendation](#movie-recommendation)
  - [Cosine Similarity](#cosine-similarity)
  - [Recommendation Function](#recommendation-function)
- [Usage](#usage)
- [Contributions](#contributions)
- [License](#license)

## Introduction

This code demonstrates how to build a content-based movie recommendation system. It uses textual data like genres, keywords, cast, crew, and overview to suggest movies similar to a given input movie.

## Getting Started

### Prerequisites

- Python 3.x
- pandas
- nltk
- scikit-learn

### Installation

1. Clone this repository:
   git clone https://github.com/amarafs99/movie-recommendation.git


## Data Preprocessing

### Merging Data

- Two datasets ('tmdb_5000_movies.csv' and 'tmdb_5000_credits.csv') are merged based on movie titles.

### Selecting Relevant Columns

- Only relevant columns, including 'movie_id,' 'genres,' 'keywords,' 'title,' 'overview,' 'cast,' and 'crew,' are selected.

### Handling Missing Data

- Rows with missing values are dropped.

### Processing Genres, Keywords, Cast, and Crew

- Text data in genres, keywords, cast, and crew columns are processed to extract names and remove spaces.

### Text Data Preprocessing

- Overview text is split into words.
- Names in cast, genres, keywords, and crew are cleaned by removing spaces.

## Feature Engineering

### Creating Movie Tags

- Movie tags are created by combining genres, keywords, overview, cast, and crew.

### Dropping Unnecessary Columns

- Unnecessary text columns are dropped.

### Text Stemming

- Text data is stemmed using the Porter Stemmer from NLTK.

### Vectorizing Text Data

- Text data is vectorized using CountVectorizer.

## Movie Recommendation

### Cosine Similarity

- Cosine similarity is used to measure the similarity between movie tags.

### Recommendation Function

- A recommendation function suggests movies similar to the input movie based on cosine similarity.

## Usage

- To use the recommendation system, call the `recommend` function with a movie name.

## Contributions

Contributions to this repository are welcome! If you find any issues or have improvements to suggest, please feel free to create a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
