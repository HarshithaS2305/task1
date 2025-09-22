dataset is taken from kaggle(https://www.kaggle.com/datasets/shivamb/netflix-shows)
the dataset contain columns(
show_id                 
type                
title              
director                
actors            
country            
date_added    
release_year             
rating
duration               
genre             
description   
we performed 
1.Ignore warnings – Prevents Python warnings from cluttering output
2.Remove duplicates – Ensures no duplicate rows exist.
3.Handle missing values
Fills missing text columns (director, cast, country, rating, description) with 'Unknown'.
Fills missing numeric columns (release_year) with median.
Fills missing dates (date_added) with a placeholder date.
4.Standardize text
Converts text to lowercase.
Standardizes type (tv show → TV Show, movie → Movie).
Standardizes rating (e.g., pg-13, tv-ma)
5.Rename columns
Converts all column names to lowercase and replaces spaces with underscores.
Example: 'listed_in' → 'genre', 'cast' → 'actors'.
6.Convert data types
Converts date_added to datetime.
Converts release_year to integer.

Output
A cleaned pandas DataFrame with:
Consistent column names
No duplicates
No missing values in key columns
Standardized text
Numeric duration in minutes
Correct data types
