# music_insight_analysis

Music Store Data Analysis is end-to-end SQL project that will help to  understand and advance their analytical skills for data analyst role

for some example like 
artists - Contains information about music artists.
Columns: artist_id, artist_name, genre
albums - Contains information about albums.
Columns: album_id, album_name, artist_id, release_date
tracks - Contains information about individual tracks.
Columns: track_id, track_name, album_id, duration, popularity
sales - Contains information about album sales.
Columns: sale_id, album_id, quantity, sale_date

SELECT a.album_name, SUM(s.quantity) AS total_sales
FROM albums a
JOIN sales s ON a.album_id = s.album_id
GROUP BY a.album_name
ORDER BY total_sales DESC
LIMIT 10;

SELECT t.track_name, t.duration, t.popularity
FROM tracks t
ORDER BY t.popularity DESC
LIMIT 10;

SELECT YEAR(a.release_date) AS release_year, COUNT(*) AS num_albums
FROM albums a
GROUP BY release_year
ORDER BY release_year;

These are just a few examples of the types of insights you can derive from a music database using SQL queries

dataset = https://drive.google.com/drive/folders/1mRUjGoOpFp9SQpT7_ToAl9TW1Hu662kv?usp=sharing
