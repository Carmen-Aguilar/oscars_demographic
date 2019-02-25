# A demographic analysis of the Oscars Awards

In February 2018 I was involved in two different stories about the lack of diversity in the Oscars Awards. 

The first analysis showed an age-gap between actors and actresses of 9 years and we reported it in the story [The anatomy of an Oscar winner](https://news.sky.com/story/anatomy-of-an-oscar-winner-11635455) published a week before the event in Hollywood. 

![age-gap.PNG](https://github.com/Carmen-Aguilar/oscars_demographic/blob/master/age-gap.PNG)

The story also deepens in the lack of gender and ethnic-balance among winners in the directing and writing categories over the 90 years of history of the Awards.  

![writingfemale.PNG](https://github.com/Carmen-Aguilar/oscars_demographic/blob/master/writingfemale.PNG)

![ethnicity.PNG](https://github.com/Carmen-Aguilar/oscars_demographic/blob/master/ethnicity.PNG)

During the weekend of the Oscars Awards, we published another analysis showing the [historical diversity problem among nominees](https://news.sky.com/story/the-oscars-and-the-problem-with-diversity-11644969). 

![genderhistoric.PNG](https://github.com/Carmen-Aguilar/oscars_demographic/blob/master/genderhistoric.PNG)

## How the analysis was done

For the first story, we considered only the winners in the six main categories: Best Actor, Best Actress, Best actor in supporting role, Best actress in supporting role, Best director and Best screenplay. Best picture was not included as it is considered a "team-prize" and it is highlight the work of a team rather than a single person and, consequently, determining gender and ethinicity would have been difficult. 

The list was taken from the [official website](http://awardsdatabase.oscars.org/) selecting the parameters required. There is an option to download the results, but the only format available is a pdf. Therefore, I scraped the website with the results using python. 

When I got the database of winners by category and year, I cleaned the names so as to get only one person per row and only the name and surname of each winner (TIP: make sure you remove spaces at the beginning and end of each name). 

I read in stackoverflow and in [the data school](https://www.thedataschool.co.uk/rachel-costa/scraping-wikipedia/) that [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) was the best option to get information about gender, date of birth and nationality of each Oscars winners. It is worth reading a bit about how wikidata works, as you need to use first the code property you are interested in and translate the codes into "understandable words".

After many loops, I used pandas to calculate the age in which each person received the award. 

<strong>Access the [Python notebook](https://github.com/Carmen-Aguilar/oscars_demographic/blob/master/OscarsAwards.ipynb) with further explanations</strong>

Once I got my database, I manually completed a couple of names where the script did not generate any result (for instance, the singer Cher). I also checked if there was any "unbelievable" data, like winners over 100 years. And, I normally take a random sample of the data and check it almost manually. 

When I was happy with my database, I changed to R to do more analysis. 

I then calculated the average age in which women and men won a statuette using the geometric mean and the ratio for categories like Best director and Best screenplay. 

<strong>[Access the R Notebook](http://rpubs.com/Carmen_Aguilar/Oscars-demographic) with the full analysis</strong>

<strong>[Download the R Notebook](https://github.com/Carmen-Aguilar/oscars_demographic/blob/master/oscarsanalysis.Rmd) with the full analysis</strong>

## Including =ImportHTML

A couple of weeks after concluding this, I was asked another analysis which included all the nominees in all the non-team categories over the 91 years of the Oscars. 

I found the list of the nominees in Wikipedia (one page for each category) and I imported them using Google Sheet and the function =ImportHTML. I combined the 17 categories considered this time in one single document and I spent hours cleaning the database in OpenRefine. 

Once I had the database, I repeated the process to get the gender parameter for each of the nominees (and winners) with wikidata. However, the ethnicity is not included in wikidata, so I used list from Wikipedia. 

I changed again to R to do the analysis (included in the R Notebook mentions above) and to export the specific data to make the visualisations.

## Visualisations

I used Datawrapper and Flourish to do the charts. 

The first story inlcudes single charts. However, I used the story option in Flourish for the second piece, which gives the possibility of accompanying the charts with text to explain what people are seeing in lines and bars. 
