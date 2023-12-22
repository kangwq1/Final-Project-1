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
