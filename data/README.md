# data

Place data file(s) in this folder.

rolling_stone <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2024/2024-05-07/rolling_stone.csv')

Then, include codebooks (variables, and their descriptions) for your data file(s)
using the following format.

## name of data file

The name of the data file is `rolling_stone`.  There are 691 observations and 21 variables.

- `variable1`: sort_name (character) - Names of musical artists/groups used for sorting.

- `variable2`: clean_name (character) - Clean names of musical artists/groups.

- `variable3`: album (character) - Names of albums on the Rolling Stone Top 500 Album list(s).

- `variable4`: rank_2003 (double) - Where each album was ranked in the 2003 list. NA if album was not released yet or not in the top 500.

- `variable5`: rank_2012 (double) - Where each album was ranked in the 2013 list. NA if album was not released yet or not in the top 500.

- `variable6`: rank_2020 (double) - Where each album was ranked in the 2020 list. NA if album was not released yet or not in the top 500.

- `variable7`: differential (double) - The difference between albums' chart placements in 2003 versus 2020. There is a negative value if it went down in the chart and a positive value if it went up.

- `variable8`: release_year (double) - The year that each album was released.
- `variable9`: genre (character) - The genre of each album.
- `variable10`: type (character) - The type of album each album is (compilation, studio, etc.).
- `variable11`: weeks_on_billboard (double) - How many weeks, if any, each album spent on the Billboard 200 album list.
- `variable12`: peak_billboard_position (double) - The peak charting position of the album on the Billboard 200 album list.
- `variable13`: spotify_popularity (double) - The popularity rank of each album on Spotify.
- `variable14`: spotify_url (character) - The Spotify URL of each album.
- `variable15`: artist_member_count (double) - The number of members in each artist/group.
- `variable16`: artist_gender (character) - The gender of each artist/group.
- `variable17`: artist_birth_year_sum (double) - The sum of the artists' birth year.
- `variable18`: debut_album_release_year (double) - What year the artist's debut album was released.
- `variable19`: ave_age_at_top_500 (double) -	The average age of the artist at Top 500 Album.
- `variable20`: years_between	(double) - Years Between the artist's debut and Top 500 Album.
- `variable21`: album_id (character) - The Album ID. NOS at the beginning of the ID if not on Spotify.

# Executive Summary


## Introduction/Dataset Background

Every several years, the Rolling Stone magazine puts out a top 500 albums list.  The first one came in 2003, then 2012, and then 2020.  The magazine curates these lists by selecting people in the music industry to vote on which albums should make the top 500 and where each one should be placed.  Each list differs from each other in album placements.  The 2020 list specifically has a completely different top ten then the two that came before it.  Part of this has to do with the voters.  "In 2003, 90% of voters were men. Not surprisingly, voters selected predominantly male performers—nearly 82% of the 500 albums selected were by men. For the 2020 ranking Rolling Stone...expanded the voting group from 269 to 336 and doubled the representation of women voters" (https://pudding.cool/2024/03/greatest-music/).  There were also more voters of color involved in the 2020 list versus the 2003 list.  I hypothesize that this also contributed drastic placement changes in the 2020 list.

## Data Information

The dataset I am using for this presentation, `rolling_stone`, has 691 observations and 21 variables.  The variables are sort_name, clean_name, album rank_2003, rank_2012, rank_2020, differential, release_year,  genre type,  weeks_on_billboard, peak_billboard_position,  spotify_popularity,  spotify_url, artist_member_count,  artist_gender artist_birth_year_sum  debut_album_release_year,  ave_age_at_top_500, and years_between	album_id.

## Research Questions

I have multiple research questions for this project. My first one is, since more women voted in 2020, are there more female artists in the 2020 list than the 2003 list and how many more are there?  My second one is, since more voters of color were added in the 2020 list, does this change reflect a difference in genres in the 2020 list and how did the genres change?  Finally and more specifically, how does the more diverse voting pool, both in terms of gender and race/genre, show in the makeup of each list's top ten?

## Methodology

First, I made separate datasets for each list: `rolling_stone_2003` and `rolling_stone_2020`.  I did this so that I could accurately visualize information that has to do with each list, and not all of the lists at once.  Next, I created some visualizations for the gender distribution of artists on each list.  For my first visualization, I used a bar graph to show the gender distribution of artists on the 2003 list.  Then I made another bar chart to show the gender distribution of artists on the 2020 list to compare the two results.  In order to show more specific data, I then displayed tables of gender counts for each list.  The first ones are only exact numbers, and the second set of tables include percentages as well.  Then, I did the same process, but for genre distribution.  Finally, I wanted to compare the top ten of each list, to show which genres and artists made the top spots.  Specifically, I wanted to show which genders and genres made the top ten.

## Findings

I found that there were more female artists and genres associated with different ethnic/racial groups in the 2020 Rolling Stones top 500 list than the 2003 list.  Between 2003 and 2020, the amount of female artists over doubled, from 7.6%, to 18.6%.  As for genres, between the 2003 and 2020 list, Hip-Hop/Rap albums, a historically Black genre, over doubled.  R&B, Funk, and Latin albums also increased.  Meanwhile, historically white genres either stayed the same, very slightly increased, or decreased on the 2020 list.  

