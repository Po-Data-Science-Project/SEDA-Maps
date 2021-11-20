# SEDA-Maps
Amy's work in progress
This is pretty final - now soliciting feedback from group members

## Overview and Motivation: Provide an overview of the project goals and the motivation for it. Consider that this will be read by people who did not see your project proposal.
We are interested in exploring the impact of educational policies and sociodemographic variation by state as predictors of student success. 
The SEDA data set provides a comprehensive picture of factors at the family, district, and state-level that we hypothesize influence student educational outcomes.

This map provides a visual comparison of the differences in per pupil expenditure and per instructor expenditure between states. Further, we wanted to explore how state education funding compares between political ideology. This was facilitated at the Congressional District level to capture the granularities unafforded when looking at state-only levels. As shown in a histogram of the distribution of scaled values, there was wide variation in the amount of funding per student and instructon by political leaning. 

Toggling between the map layers, provides a visual of the geographic distribution of Congressional Districts lines and spending on education by political leaning.

## Related Work: Anything that inspired you, such as a paper, a web site, or something we discussed in class.
This work was inspired by the redrawing of Congressional boundary lines based on the 2020 Census. Gerrymandering is threat to democracy and has serious real-world consequences. When districts are drawn unfairly, the public is prevented from electing representatives that accurately reflect the views of the population. Most often marginalized groups are redistributed to minimize their voices and votes. 

## Initial Questions: What questions are you trying to answer? How did these questions evolve over the course of the project? What new questions did you consider in the course of your analysis?
Here this work underscores the potential impact on students and teachers by visualizing current differences in spending in education for grades 3-8 based on the dominant political ideology in Congressional Districts. This question arose as way to compare the two major parties – Democrats and Republicans – to illuminate how political platforms and values have direct impacts at the level of school districts. An overview of the party education platforms are included. 

## Data: Source, scraping method, cleanup, etc.
Sources: 
- The American Ideology Project (2015 update), available from: https://americanideologyproject.com/
- Stanford Education Data Archive, (codebook_covariates_v1_1.xlsx), avaible from: https://exhibits.stanford.edu/data/catalog/db586ns4974
- 113th Congressional District coordinates, availabe from: https://github.com/ropensci/USAboundaries

## Exploratory Analysis: What visualizations did you use to look at your data in different ways? What are the different statistical methods you considered? Justify the decisions you made, and show any major changes to your ideas. How did you reach these conclusions?
The first step was to delineate between political right and left Congressional Districts. We used included estimates of political preferences from a collection of survey measures to capture the distribution of political preferences based on the citizens (Tausanovitch and Warshaw, 2013). As mentioned above, one concern we had was that, as a result of gerrymandering, relying only on the election results and the parties of Congressional representatives may underweight the true distribution of political preferences by those living in the District.  
Next, we collapsed school districts into their respective Congressional Districts, averaging the per pupil expenditure and per instructor expenditure for a single measure per Congressional District. 

To visualize if the distribution of education spending differed by politcal ideology, we included a histogram of the scaled measures. From the histogram, we find that, indeed, confirms our hypothesis: that based on party platforms, Republican majority districts would invest less in students and teachers. The mean and variance of spending is different by right and left leaning districts, with districts that are more left-leaning, on average, investing more in students and teachers with a right skew (meaning there are more districts that invest more in students and teachers). 

## Final Analysis: What did you learn about the data? How did you answer the questions? How can you justify your answers? Note that 1 type of analysis per team member is required. A Shiny app counts as a type of analysis.
This was a very interesting analysis. First, through the opensource work by The American Ideology Project, was the analysis even possible. A measure of constituent political preferences by Congressional District based on a wide breadth of surveys, election results among othres, afforded an analytical depth of how the individual voter political preferences is one component when considering differences in school district support and student outcomes.
It is clear, that investing in students and teachers to ensure that all can access the support needed is critical for equity in education. We find that despite that the for right-leaning Districts, the magnitude in which constituent preferences are predominantly conservative is much greater than for left-leaning Districts. In other words, Districts that are more left-leaning, are less radically liberal (and more neutral) than right-leaning Districts are radically conservative. 
Yet, left leaning districts invest more on average in students and teachers, with the leading Districts left-leaning.
Further, follow up analyses may want to look at other outcomes, such as student teacher ratio and proportions of special education students, english language learners, special education teachers, and guidance counselors in school districts between Congressional Districts. 
