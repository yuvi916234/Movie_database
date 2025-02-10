**Movie Database Management System
**
**Overview
**
This project provides a structured SQL database schema for a Movie Database Management System. It includes tables for movies, actors, actresses, directors, reviews, genres, and box office collections, with proper relationships using primary and foreign keys. The database also contains stored procedures, views, and triggers to streamline data retrieval and manipulation.

**Features
**
Movies, Actors, Actresses, and Directors Management

Many-to-Many Relationships for actors and actresses appearing in multiple movies

Movie Reviews and Ratings System

Genre Classification for better categorization

Box Office Collection Tracking

Stored Procedures for Data Retrieval

Triggers for Auto-Updating Ratings and Review Counts

Views for Quick Movie Collection Insights

**Database Schema
**
**Tables:
**
movies - Stores movie details.

actors - Stores actor information.

actresses - Stores actress information.

directors - Stores director details.

movie_actors - Junction table to link movies and actors.

movie_actresses - Junction table to link movies and actresses.

movie_directors - Junction table to link movies and directors.

reviews - Stores movie reviews and ratings.

genres - Stores movie genres.

movie_collection - Stores box office collection details.

**Stored Procedures
**
ratings_and_reviews(IN p_movie_id INT): Fetches average ratings and total reviews for a movie.

GetMoviesByYear(IN release_year INT): Retrieves movies released in a specific year.

SearchMoviesByRating(IN min_rating DECIMAL(2,1)): Lists movies with an average rating above the specified value.

SearchMoviesByGenre(IN genre_name VARCHAR(20)): Lists movies that belong to a particular genre.

**Views
**
mov_det: Displays movie details along with box office collection, days run, and opening day revenue.

**Triggers
**
update_total_ratings: Automatically increments total ratings when a new review is inserted.

update_avg_rating: Recalculates the average rating when a new review is inserted.

**How to Use
**
1. Clone the Repository

git clone https://github.com/yourusername/movie-database.git
cd movie-database

2. Import the Database

Execute the movie_database.sql script in your MySQL database.

SOURCE movie_database.sql;

3. Query the Database

Use stored procedures to retrieve data:

CALL GetMoviesByYear(2023);
CALL SearchMoviesByRating(8.0);
CALL SearchMoviesByGenre('Action');

**Contributing
**
Feel free to submit pull requests or open issues to suggest improvements or add new features.

**License
**
This project is licensed under the MIT License.

This README provides a structured guide to the Movie Database Management System, making it easier for contributors and users to understand and use the database effectively.

