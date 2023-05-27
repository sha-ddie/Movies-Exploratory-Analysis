# Most Profitable Movie Types, Top Movie Studios and Production Crews.

![pictue](data/film-production.jpg)
Photo was obtained [here](https://academy.wedio.com/filmmaking)

## Introduction
***
Film production began in 1900 by [Charles Pathé](https://en.wikipedia.org/wiki/Charles_Path%C3%A9), while the first film theatre to be introduced was "The Nickelodeon" in Pittsburgh(United States) 1905. Since then, film production and theaters have increased spontaniously till the 20th centuary, where film industry worldwide has revenue of around 77B, [Statista](https://www.statista.com/topics/5431/film-production-worldwide/#topicOverview). The revenue genereted from Movies is usually accumulated from the following sources ;
- Merchandising
- Television Broadcats
- Home video
- Theatre Exhibitions.

However, out of all these sources theatre exhibitions (aka box office) is the most used measure to asses the  the success of a movie, because of data availability compared to the other revenue sources.
Movies produced are usually categorised according to the style, theme or scenes associated with the movie, such categories are called **genres**, few examples of movie genres are **Actio, Thriller, Drama, Horror and Comedy**.  

## Problem Statement
***
In light with the high revenues accrued by the film industry over the years, which is forcasted to keep on rasing , has made movie studios to accumulate high profits from movie production in for of reveue.  As a result Microsoft, a renowed multinational software production company, has decided to tap into the profits and venture in movie production by become a copmetitive movie production studio. To address this we will be investigating the best selling movie types in the box offices and the production line Microsoft should aline with top inorder to top the tables as one of the best movie studio in the recent future.

## Main Objective
***
Our main problem, in this project, is to investigate the best selling movie types, the best movie production crews and the top movie production studios.


## Metric for Success
***
To provide actionable insights on profitable movie types to venture into and lists of best rated production crews and top movie production studios that Microsoft can use in its new studio.


## Specific Objectives
***
* To identify the movie genres / types that produce high gross income in box offices that Microsoft studio can specialise in production  

* To list the top professionals ( Producers, Actors, Directors) who can be  considered for hire, and are linked to the most  high grossed movies

* To list the best movie production studios that have a  movie gross incomes that Microsoft studio could partner with in production


## Data Understanding
***
The datasets used in this project were sourced from various movie databases and website such as [TheMovieDB](https://www.themoviedb.org/) , [IMDB](https://www.imdb.com/) and [Rotten Tomatoes](https://www.rottentomatoes.com/). They contain various attributes of intrests such as movie: ***titles , gross sales , production studios , year of production , produers , actors*** and **directors*** .  
The datasets that have been used are;
> The `bom.movie_gross.csv`, where each row represents a particular movie and its corresponding attribute. The data set contains 3387: movies and 5: movie atributes which include; `title`, `studio`, `domestic_gross`, `foreign_gross` and `year`.

> The `im.db` is SQLite database of IMDB data, that contain 8 tables that are link together using primary and foreign keys. Each table contains different information corresponding to particular movie title and movie id  found in the `movie_basics` table. From this  database we are going to create two tables which will contain the requred attrubutes:
- `movie_basics` table, which is a join of the `movie_basics` and `movie_ratings` tables and will have the following attributes {`movie_id`, `runtime_minute`, `primary_title` and `genres`}

- `persons` table, which is a join of the  `persons` and `principlas` tables inorder to have the following attributes {`person_id` , `primary_name`, `movie_id` and  `category`}

## Data Preparation
***
The data was checked for missing values duplicates and placeholders of missing data. The missing values were handled by dropping all the rows with them while duplicates were not found in our data. New columns created from transforming existing columns and those columns that were not in their appropriate data type were cleaned and converted into their approbriate data type 

## Data Analysis
***
Form the analysis, the following visualizations about the most selling movie genres and the top prouction studios were ;  
![](data/analysis.png)
For preview of the complete analysis process , here is the link to the [Notebook](https://github.com/sha-ddie/Phase-1-Project/blob/main/Student.ipynb)

## Conclusions
***
- The top most selling movie types / mixed-genres are; 
     - Action, Adventure, Sci-fi
     - Action, Adventure,  Fantasy
     - Action, Adventure, Thriller
     - Action, Adventure, Comedy
     - Adventure, Animation, Comedy 
     - Action, Adventure, Animation
     
- The best experienced movie producers of the above mixed-genres as per the available data were ;
    > Janet Healy , Kevin Feige , Ian Bryce , Darla K. Anderson , Tom DeSanto , Don Murphy , Kathleen Kennedy , Simon Kinberg , Christopher Meledandri and Lorenzo di Bonaventura 
    
- The best experienced movie directors as per the available data were ;
    > Kyle Balda , Pierre Coffin , Sam Mendes , Brad Bird , Michael Bay , Lee Unkrich , Chris Renaud , Anthony Russo , Joe Russo and James Gunn

- The best experienced movie actors as per the available data were are ;
    > Michael Keaton , Steve Carell , Robert Downey Jr. , Javier Bardem , Geoffrey Rush , Don Cheadle , Kevin Hart , Jason Momoa , Chris Pratt and Stanley Tucci
    
- The top best movie producing studios as per the available data were ;
    - BV   - Buena Vista Pictures AKA ( Walt Disney Studios Motion Pictures)
    - WB   -   Warner Bros. Entertainment 
    - Uni.   -   Universal Pictures
    - Par.   -   Paramaount Pictures
    - Sony   -   Sony Pictures

## Recommendations
***
- 1: The shoudld specialise its movie production in the following mixed-genres ; { (Action, Adventure, Sci-fi) , (Action, Adventure,  Fantasy ) , ( Action, Adventure, Thriller ) , ( Action, Adventure, Comedy) , ( Adventure, Animation, Comedy) , ( Action, Adventure, Animation ) }
***
- 2: The company should consider the list of producers for their movie productions ;  [Janet Healy , Kevin Feige , Ian Bryce , Darla K. Anderson , Tom DeSanto , Don Murphy , Kathleen Kennedy , Simon Kinberg , Christopher Meledandri and Lorenzo di Bonaventura ]
***
- 3: The company should consider the folloeing list of directors to corrdinate their movie productions ; [ Kyle Balda , Pierre Coffin , Sam Mendes , Brad Bird , Michael Bay , Lee Unkrich , Chris Renaud , Anthony Russo , Joe Russo and James Gunn ] 
***
- 4: The company should consider this list of actors to be theri lead actors during movie productions ; [ Michael Keaton , Steve Carell , Robert Downey Jr. , Javier Bardem , Geoffrey Rush , Don Cheadle , Kevin Hart , Jason Momoa , Chris Pratt and Stanley Tucci ] 
***
- 5: In case of a partneship in movie production th company should consider the folloeing list of production studios ; [ ( Walt Disney Studios Motion Pictures) , (Warner Bros. Entertainment ) , ( Universal Pictures) , (Paramaount Pictures ) , (Sony Pictures) ]


