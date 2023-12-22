# Final-Project-1
Hands-on Lab: Final Project (Introduction to Hands-on Lab: Final Project)

#Task 1 
library(httr)
library(rvest)

get_wiki_covid19_page <- function() {
  wiki_base_url <- "https://en.wikipedia.org/w/index.php"
  url_parameter <- "title=Template:COVID-19_testing_by_country"
  full_url <- paste(wiki_base_url, "?", url_parameter, sep = "")
  response <- httr::GET(url = full_url)
  return(response)
}

## error code displayed is shown below
File "/tmp/ipykernel_481/3996746759.py", line 3
    get_wiki_covid19_page <- function() {
                                        ^
SyntaxError: invalid syntax


## Alternative code for same task 
get_wiki_covid19_page <- function() {
wiki_base_url <-  "https://en.wikipedia.org/w/index.php"
wiki_params <- list(title = "Template:COVID-19_testing_by_country")
response <- GET(wiki_base_url, query = wiki_params)
return(response)
}

## still getting same kind of syntax errors with code above
   
