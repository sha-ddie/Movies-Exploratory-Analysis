# Movie Attributes That Contribute to High Box Office Revenues.

![pictue](images/film-production.jpg)
Photo was obtained [here](https://academy.wedio.com/filmmaking)

## Introduction
***
Film production began in 1900 by [Charles Pathé](https://en.wikipedia.org/wiki/Charles_Path%C3%A9), while the first film theatre to be introduced was "The Nickelodeon" in Pittsburgh(United States) 1905. Since then, film production and theaters have increased spontaneously till the 20th century, when the film industry worldwide has revenue of around 77B, [Statista](https://www.statista.com/topics/5431/film-production-worldwide/#topicOverview). The revenue generated from Movies is usually accumulated from the following sources ;
- Merchandising
- Television Broadcast
- Home video
- Theatre Exhibitions.

However, out of all these sources theatre exhibitions (aka box office) is the most used measure to assess the success of a movie, because of data availability compared to the other revenue sources.
Movies produced are usually categorized according to the style, theme, or scenes associated with the movie, such categories are called **genres**, few examples of movie genres are **Action, Thriller, Drama, Horror, and Comedy**.  

## Problem Statement
***
In light with the high revenues accrued by the film industry over the years, which is forecasted to keep on rising, has made movie studios accumulate high profits from movie production in for of revenue.  As a result Microsoft, a renowned multinational software production company, has decided to tap into the profits and for the first time to venture into movie production by starting a movie production studio. To address this we will be investigating the best-selling movie types in the box offices and the top production crew that Microsoft should aline with in order high box office revenues.

### c) Main Objective
***
This project aims to identify the best-selling movie types, the best-experienced movie production crews, and the top movie production studios that could guide Microsoft as they venture into movie production.


### d) Metric for Success
***
Providing actionable insights on profitable movie types to venture into and lists of best-experienced production crews and top movie production studios that Microsoft can adhere with in its new studio.


### e) Specific Objectives
***
* To identify the movie types / genres that produce high gross income in box offices that Microsoft studio can specialize in production  

* To list the top experienced professionals ( Producers, Actors, Directors) who are linked to the most high-grossed movies

* To list the best movie production studios that have high movie gross incomes that Microsoft Studio could partner with in production


## Data Understanding
***
The datasets used in this project were sourced from various movie databases and websites such as [TheMovieDB](https://www.themoviedb.org/), [IMDB](https://www.imdb.com/), and [Rotten Tomatoes](https://www.rottentomatoes.com/).The movie attributes of interest in our analysis are : ***movie titles , gross sales , production studios, producers, actors*** and **directors*** . The attributes are contained in two datasets namely; 

> The `bom.movie_gross.csv` which has 3387 movies (rows) and 5 movie attributes (columns). Each row represents a particular movie and its corresponding attribute, that is ; `title`, `studio`, `domestic_gross`, `foreign_gross` and `year`.

> The `im.db` is an SQLite database of IMDB data, that contains 8 tables that are linked together using primary and foreign keys. Each table contains different information corresponding to a particular movie title and movie_id  found in the `movie_basics` table. From this  database we are going to extract two tables:
- `movie_basics` table, which is a join of the `movie_basics` and `movie_ratings` tables and will have the following attributes {`movie_id`, `runtime_minute`, `primary_title` and `genres`}

- `persons` table, which is a join of the  `persons` and `principlas` tables and will have the following attributes {`person_id` , `primary_name`, `movie_id` and  `category`}

## Data Preparation
***
The data was checked for missing values duplicates and placeholders of missing data. The missing values were handled by dropping all the rows with them while duplicates were not found in our data. New columns were created from transforming existing columns and those columns that were not in their appropriate data type were cleaned and converted into their appropriate data type 

## Data Analysis
***
From the analysis, the following visualizations about the most-selling movie genres and the top production studios were ;  
![](images/analysis.png)
For a preview of the complete analysis process, here is the link to the [Notebook](https://github.com/sha-ddie/Phase-1-Project/blob/main/Student.ipynb)

## Conclusions
***
- The topmost-selling movie types / mixed-genres are; 
     - Action, Adventure, Sci-fi
     - Action, Adventure,  Fantasy
     - Action, Adventure, Thriller
     - Action, Adventure, Comedy
     - Adventure, Animation, Comedy 
     - Action, Adventure, Animation
     
- The best-experienced movie producers of the above mixed-genres as per the available data were ;
    > Janet Healy , Kevin Feige , Ian Bryce , Darla K. Anderson , Tom DeSanto , Don Murphy , Kathleen Kennedy , Simon Kinberg , Christopher Meledandri and Lorenzo di Bonaventura 
    
- The best-experienced movie directors as per the available data were ;
    > Kyle Balda , Pierre Coffin , Sam Mendes , Brad Bird , Michael Bay , Lee Unkrich , Chris Renaud , Anthony Russo , Joe Russo and James Gunn

- The best-experienced movie actors as per the available data were are ;
    > Michael Keaton , Steve Carell , Robert Downey Jr. , Javier Bardem , Geoffrey Rush , Don Cheadle , Kevin Hart , Jason Momoa , Chris Pratt and Stanley Tucci
    
- The top best movie producing studios as per the available data were ;
    - BV   - Buena Vista Pictures AKA ( Walt Disney Studios Motion Pictures)
    - WB   -   Warner Bros. Entertainment 
    - Uni.   -   Universal Pictures
    - Par.   -   Paramount Pictures
    - Sony   -   Sony Pictures

## Recommendations
- 1: The company should specialise its movie production in the following mixed-genre: (Action, Adventure, Sci-fi) 
***
- 2: The company should consider the list of producers for their movie productions ;  [Janet Healy , Kevin Feige , Ian Bryce , Darla K. Anderson , Tom DeSanto , Don Murphy , Kathleen Kennedy , Simon Kinberg , Christopher Meledandri and Lorenzo di Bonaventura ]
***
- 3: The company should consider the following list of directors to coordinate their movie productions ; [ Kyle Balda , Pierre Coffin , Sam Mendes , Brad Bird , Michael Bay , Lee Unkrich , Chris Renaud , Anthony Russo , Joe Russo and James Gunn ] 
***
- 4: The company should consider this list of actors to be their lead actors during movie productions ; [ Michael Keaton , Steve Carell , Robert Downey Jr. , Javier Bardem , Geoffrey Rush , Don Cheadle , Kevin Hart , Jason Momoa , Chris Pratt and Stanley Tucci ] 
***
- 5: In case of a partnership in movie production the company should consider Walt Disney Studios Motion Pictures. 

## Resources.
1: For the complete notebook analysis, here is the [Notebook](https://github.com/sha-ddie/Phase-1-Project/blob/main/Student.ipynb)
2: The Presentation slides are found [here](https://www.canva.com/design/DAFkG9L58Po/eo4fBJwhsaUeclYPNNmS4w/view?utm_content=DAFkG9L58Po&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink)