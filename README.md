# netflix_sql_project
![netflix logo]{https://github.com/Vaibhavsharma9528/netflix_sql_project/blob/main/logo.png}

# 🎬 Netflix Data Analysis Using SQL

This project performs an in-depth analysis of Netflix's content library using SQL. By exploring a dataset containing information on Netflix's movies and TV shows, the goal is to derive actionable insights on content distribution, popular genres, ratings, and trends across different time periods.

## 📁 Dataset

The dataset used in this analysis is the [Netflix Titles Dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows), which includes a list of Netflix movies and TV shows with attributes such as:

- Title
- Type (Movie/TV Show)
- Director
- Cast
- Country
- Release Year
- Rating
- Duration
- Genre (listed_in)

## 🛠️ Technologies Used

- **PostgreSQL**: For querying and storing the data.
- **pgAdmin**: Used to manage the PostgreSQL database.
- **SQL**: Structured Query Language for data analysis.

## 🔍 Key SQL Queries & Insights

Here are some of the core SQL queries that provide insights into Netflix’s content:

### 1. **Most Common Rating for Movies and TV Shows**
   - Analyzes the distribution of ratings across content types (TV shows and movies).

### 2. **Movies Released in 2020**
   - Retrieves a list of movies added to Netflix in 2020.

### 3. **Top 5 Countries with the Most Content**
   - Identifies the top 5 countries producing the most Netflix content.

### 4. **Longest Movie**
   - Finds the movie with the longest duration.

### 5. **Content Added in the Last 5 Years**
   - Filters the content added to Netflix in the past 5 years.

### 6. **Count of TV Shows vs. Movies**
   - Breaks down Netflix's library by TV shows and movies.

### 7. **Most Common Genres**
   - Lists the most popular genres on Netflix by the number of titles in each genre.

### 8. **Monthly Trend of Content Added (Last 2 Years)**
   - Shows the monthly content addition trend over the past 2 years.

## 📊 Data Exploration Example

The following SQL queries were used to derive insights about Netflix's global content:

```sql
-- Most common ratings for movies and TV shows
SELECT rating, COUNT(*) AS total
FROM netflix
GROUP BY rating
ORDER BY total DESC;
````

```sql
-- Top 5 countries with the most content
SELECT country, COUNT(*) AS total
FROM netflix
WHERE country IS NOT NULL
GROUP BY country
ORDER BY total DESC
LIMIT 5;
```

### 🗺️ Key Insights

* **Rating Distribution**: The most common rating for Netflix content is **TV-MA**.
* **Country Distribution**: The United States produces the highest number of Netflix titles.
* **Content Addition**: Netflix's content addition rate has surged significantly after 2018, especially in the non-English-speaking markets.

## 🚀 How to Run

### 1. **Set Up the Database**

* Download the **Netflix Titles Dataset** from Kaggle.
* Import the dataset into a PostgreSQL database using pgAdmin or any PostgreSQL client.
* Ensure that the table is properly created and the data is loaded.

### 2. **Running SQL Queries**

* Open pgAdmin or a PostgreSQL client.
* Run the provided SQL queries to explore the dataset and derive insights.
* Modify or extend the queries as needed for deeper analysis.


## 💻 How to Contribute

Feel free to fork the repository, contribute enhancements, or open issues if you have suggestions for improving the project.

### How to contribute:

1. Fork this repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request when you’re ready for your changes to be reviewed.

## 📌 License

This project is for **educational purposes only**.

---

### 🤝 Acknowledgements

* **Kaggle** for providing the Netflix dataset.
* **PostgreSQL** for enabling efficient querying and analysis of large datasets.

---



