# overview of skills to progress
##  foundational data science skills in R


- Basic visualizations: bar charts, line charts, histograms
- Manipulating colors in charts
- Visualization formatting (I.e., how to format your charts to make them look good)
- String manipulation
- Date manipulation
- Data reshaping (I.e., transforming from ‘wide’ format to ‘long’ format and visa-versa)
- Adding variables
- Removing variables
- Aggregating data
- Reading in data (from external sources)
- Working with factor variables (e.g., ordering factors, re-naming factor levels, re-categorizing factor variables, etc)
  
  

# exploring data exploratory analysis

## principles
1. What type of variation occurs within my variables?
2. What type of covariation occurs between my variables?


# wk 5 lecture notes - data summaries + Tweets walkthrough

## data file RDS format notes
save to RDS format example -- e.g. save a tweet search into a RDS file
- any R object can be saved to this
- binary cache of the object it seems

## dplyr :: summarise()
- always try mix of:
	- View(), dim(), str(), summary(), glimpse()!
- summary stats 
	- n() , min() , quantile(), mean() etc
	- creates a table with columns going by the params you pass it 
	- need to get rid of NAs usually, so use na.rm = TRUE parameter
- can use pipeline syntax for data in the function, e.g. tweets %>% summarise(...)
- worth using a n = n() always just to sensecheck observations used
- also run a glimpse() call on the summary afterward


### handling NAs
- various ways in this : see -- https://mareds.github.io/r_course/lecture06_data_wrangling_tidy_data.html#39 & see https://www.rstudio.com/resources/cheatsheets/
- which() function good for attending to extreme values or those of interest
	- id <- which(cruise$station_1 == max(cruise$station_1))

# wk6 data relations (and wk7)
Joins and pipes -- so dplyr package mostly

Fine reference for this in easy terms: https://anderfernandez.com/en/blog/dplyr-tutorial/
- grouping : group_by or ungroup 
- 