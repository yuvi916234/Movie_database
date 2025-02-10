Movie Database Management System

•	Overview:
        This project provides a structured SQL database schema for a Movie Database Management System. It includes tables for movies, actors, actresses, directors, reviews, genres, and box office collections, with proper relationships using primary and foreign keys. The database also contains stored procedures, views, and triggers to streamline data retrieval and manipulation.

•	Features:
      1.	Movies, Actors, Actresses, and Directors Management
      2.	Many-to-Many Relationships for actors and actresses appearing in multiple movies
      3.	Movie Reviews and Ratings System
      4.	Genre Classification for better categorization
      5.	Box Office Collection Tracking
      6.	Stored Procedures for Data Retrieval
      7.	Triggers for Auto-Updating Ratings and Review Counts
      8.	Views for Quick Movie Collection Insights
      9.	Database Schema

•	Tables:
      1.	movies - Stores movie details.
      2.	actors - Stores actor information.
      3.	actresses - Stores actress information.
      4.	directors - Stores director details.
      5.	movie_actors - Junction table to link movies and actors.
      6.	movie_actresses - Junction table to link movies and actresses.
      7.	movie_directors - Junction table to link movies and directors.
      8.	reviews - Stores movie reviews and ratings.
      9.	genres - Stores movie genres.
      10.	movie_collection - Stores box office collection details.

•	Stored Procedures:

      1.	ratings_and_reviews(IN p_movie_id INT): Fetches average ratings and total reviews for a movie.
      2.	GetMoviesByYear(IN release_year INT): Retrieves movies released in a specific year.
      3.	SearchMoviesByRating(IN min_rating DECIMAL(2,1)): Lists movies with an average rating above the specified value.
      4.	SearchMoviesByGenre(IN genre_name VARCHAR(20)): Lists movies that belong to a particular genre.

•	Views

      mov_det: Displays movie details along with box office collection, days run, and opening day revenue.

•	Triggers
      1.	update_total_ratings: Automatically increments total ratings when a new review is inserted.
      2.	update_avg_rating: Recalculates the average rating when a new review is inserted.

•	How to Use:

      1. Clone the Repository
      git clone https://github.com/yourusername/movie-database.git
      cd movie-database
      
      2. Import the Database
      Execute the movie_database.sql script in your MySQL database.
      SOURCE movie_database.sql;
      
      3. Query the Database
      Use stored procedures to retrieve data:
      CALL GetMoviesByYear(enter a year);
      CALL SearchMoviesByRating(enter a rating);
      CALL SearchMoviesByGenre('enter a genre');
