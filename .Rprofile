.First <- function(){
  # options(java.parameters = "-Xmx4g" )
  
  options(Hverbose=FALSE)
  
  x<-c("Hmisc","ggplot2","tidyverse","RPostgreSQL","readr","RJDBC","rJava","lubridate","DBI","RColorBrewer","dplyr")
  lapply(x, require, character.only = TRUE)

  options(dplyr.jdbc.classpath = "/Users/msullivan2/Documents/snowflake-jdbc-3.9.1.jar")
  library("dplyr.snowflakedb")

  # this adds /usr/texbin to the R path
  Sys.setenv(PATH=paste(Sys.getenv("PATH"),"/usr/texbin",sep=":"))

  # Change this to your ocrem directory
  setwd("/Users/msullivan2/Documents/GitHub/sandbox/sandbox/")

  # # Load depot bootstrap for generic functions
  # for (file in list.files("/Users/msullivan2/Google Drive MFP/projects/R setup/functions", NULL, FALSE, TRUE)) {
  #   source(file)
  # }

  # Load all of the R functions
  for (file in list.files("./functions", ".R$", FALSE, TRUE, TRUE)) {
    source(file, chdir = TRUE)
  }

  updatePrompt <- function(...) {options(prompt=paste(Sys.time(),"> ")); return(TRUE)}
  addTaskCallback(updatePrompt)

options(scipen=999)

# blue,orange,navy,red,yellow,green, med blue 1, turquoise, med blue 2, light orange, med orange, dark orange
#https://www.viget.com/articles/add-colors-to-your-palette-with-color-mixing/
katescolor <<- c("#138AB1","#EF601E","#0F354B","#b8281b","#e8c03c","#98af61","#10516d","#529d88","#126d8e","#e9a031","#ed7f27","#d4441d")



}
