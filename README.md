# TMDb Dataset Investigation
## by Ryan Sikhrangkur

## TMDb Dataset Overview

The dataset contains more than 10,000 movies collected independently by The Movie Database, with titles released as early as 1960 until 2015.

There are 21 columns of data for each movie:
> id
> imbd_id
> popularity
> budget
> revenue
> original_title
> cast
> homepage
> director
> tagline
> keywords
> overview
> runtime
> genres
> production_companies
> release_date
> vote_count
> vote_average
> release_year
> budget_adj
> revenue_adj
   
Additionally there were notes included in regards to some columns:
> 1. Columns such as genres, cast, director and production_companies have multiple names/values stored in a run-on str value with a | character to act as a separator.
> 2. The budget_adj and revenue_adj are included to adjust the budget and revenue columns respectively to how these values would be if the movie released in the year 2010 to reflect rising costs in the film industry.

## Questions to Ask

I drafted two primary questions to have the dataset answer: what movies had the highest revenue (before and after the 2010 release_year), and which directors had the highest popularity. Considering these questions, and the reasons or information behind the answers, helped focus what was important for cleaning the data.

## V1 vs. V2

The journal and HTML files labeled V1 is the project state as it was originally submitted for Udacity's Data Analysis nanodegree program. In the cleaning process I removed all films which reported a 0 for revenue or budget, resulting in a large reduction of films from 10,866 to 3,805. I retrieved the top 10 films before and after 2010 (20 total), and the five most popular directors.

V2 is my independent revisit of the project to better improve the steps taken since I originally submitted it. Rather than removing all movies which reported a 0 in budget or revenue, I changed their values to the average instead. After removing movies for still having missing data crucial to my questions, the size was reduced to 9,772. To better reflect the massive quantity, I expanded the size of my results to 25 movies before and after the 2010 release_year (50 total), and 10 directors.