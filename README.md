# A demographic analysis of the Oscars Awards

In February 2018 I was involved in two different stories about the lack of diversity in the Oscars Awards. 

The first analysis showed an age-gap between actors and actresses of 9 years and we reported it in the story [The anatomy of an Oscar winner](https://news.sky.com/story/anatomy-of-an-oscar-winner-11635455) published a week before the event in Hollywood. 

IMG

The story also deepens in the lack of gender and ethnic-balance among winners in the directing and writing categories over the 90 years of history of the Awards.  

IMG

IMG

During the weekend of the Oscars Awards, we published another analysis showing the [historical diversity problem among nominees](https://news.sky.com/story/the-oscars-and-the-problem-with-diversity-11644969). 

IMG

## How the analyses was done

The first story narrowed down the analysis to the winners in the six main categories. Best Actor, Best Actress, Best actor in supporting role, Best actress in supporting role, Best director and Best screenplay. Best picture was not included as it is considered a "team-prize" where is not highlihting the work of a single person and, consequently, determining gender and ethinicity would have been difficult. 

The list was taken from the [official website](http://awardsdatabase.oscars.org/) selecting the parameters required. There is an option of downloading the results, but the only format available is a pdf. Therefore, I scraped the website with the results using python. 

When I got the database of winners by category and year, I added the gender, the year of birth and the nationality for each one using [wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page).  
