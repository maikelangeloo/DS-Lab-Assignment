# DS-Lab-Assignment

## Dataset
Name: top_100_spotify_songs_2025
Source: Kaggle

## Steps Performed
- Loaded dataset
- Examined structure and summary statistics
- Checked missing values
- Visualized distributions and relationships

## Tools Used
- R
- tidyverse
- ggplot2

## R Code
install.packages("tidyverse")
install.packages("ggplot2")

library(tidyverse)
library(ggplot2)

data <- read.csv("LAB DATA EDA/DATASET/top_100_spotify_songs_2025.csv")

str(data)

head(data)

summary(data)

colSums(is.na(data))

ggplot(data, aes(x = Spotify_Streams_Millions)) + geom_histogram(bins = 30)

ggplot(data, aes(y = Spotify_Streams_Millions)) + geom_boxplot()

cor(select_if(data, is.numeric))
