# Generating giveaway winners

## Background Overview
As part of a social media marketing campaign for my small handcrafted jewelry business, I hosted a giveaway on Instagram where three participants will be randomly selected to win free earrings. Participants enter by filling out a market survey form (code for survey's data analysis in another repository).

Participants may also tag other Instagram accounts in the cooments section, with one tag representing an **extra** entry in the giveaway. I received ~1000 comments, with some participants tagging up to 20 different accounts.

## Problem Statement
In order to fairly generate three winners, there are a few things to do: 
1. Export ~1000 Instagram comments as a readable file
2. Clean data and extract relevant information
3. Total up each participant's entry count (1 for survey + n accounts tagged)
4. Running a random generator over all giveaway entries

## Approach
Following converting all comments into a CSV file, I utilized string manipulation and iteration to search for the '@' character in order to sum up the number of accounts tagged per participant. I generated three winners by using the random.choice method fromm NumPy. 
