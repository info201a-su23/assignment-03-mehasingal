# A2: U.S. COVID Trends

## Overview
In many ways, we have come to understand the gravity and trends in the COVID-19 pandemic through data. Regardless of media source, people are consuming more epidemiological information than ever, primarily through reported figures, charts, and maps.

This assignment is your opportunity to work directly with the same data used by the [New York Times](https://github.com/nytimes/covid-19-data/). While the analysis is guided through a series of questions, it is your opportunity to use programming skills to ask more detailed questions about the pandemic.

## Getting Started
You should start this assignment by opening up the `analysis.R` script. The script will guide you through an initial analysis of the data.

* **Coding prompts.** Complete the coding prompts in `analysis.R`. You MUST use the `dplyr` package.

* **Reflection prompts.** Throughout `analysis.R`, there are prompts labeled `"Reflection"`. Please write at least 1-3 sentences for each of these prompts below in this `README.md` file. As appropriate, provide evidence, give justification for your opinions, or genuinely reflect on your views. Please strive for concise, clear, and interesting writing.

## Reflection 1
Before actually calculating the total number of COVID cases and deaths, record your guesses for the following questions.

Guess: How many total COVID cases do you think there have been in the U.S.?

I think there have been about 50 million cases in the U.S

Guess: How many total COVID-related deaths do you think there have been in the U.S.?

I think there have been about 2-3 million COVID-related deaths in the US. 

Guess: Which state do you think has the highest number of COVID cases, and which state do you think has the lowest?

I think New York or California had the highest number of COVID cases and I think the state with the lowest would be a more rural, less populated state like Wyoming. 

## Reflection 2
Did the number of COVID cases and deaths surprise you? Why or why not? What about the states with the highest and lowest number of cases? How did your guesses line up with the actual results? Answer in at least 1-3 sentences

The number of COVID cases and deaths using the 'national' data set did 
actually surprise me because of how low the death count seemed. The total US 
deaths, based on that specific data set, was 1,115,001, which when compared
to the amount of total cases (100 million) seems quite insignificant and less
than what I thought. The state with the highest number of cases matched with
my guess, which was either California or New York due to their population 
size.The state with the lowest number of cases did actually surprise me 
because I didn't think about the inclusion of U.S territories and islands
off the mainland, like American Samoa which turned out to have the lowest
number of COVID cases. This makes sense due to their isolated environment
and small population. 

## Reflection 3
Which county has the highest number of cases in the state of Washington, and does it surprise you? Why or why not? (You may need to google this county to learn about it) Answer at least in 1-3 sentences

The county that has the highest number of cases in the state of Washington,
based on the highest cases in each state data frame that I made is King County.
This does not surprise me at all; King County is the most populous county in
WA, as it ranges from Seattle, to the Eastside, and all the way to Renton.
Some of the earliest cases of COVID in the United States was actually
reported in King County, making it a hot spot for cases since 2020. 

## Reflection 4
Why are there so many observations (counties) in the variable `lowest_deaths_in_each_state`? That is, wouldn't you expect the number to be around 50? Why is the number greater than 50? Answer in at least 1-3 sentences

There are so many observations in the data frame, lowest deaths in each
state because there are "ties" for multiple counties
(and even repeats of the same county) with the same lowest death count,
which was 0, typically from "Unknown" counties where there may have been
no clear boundaries or poor reporting on deaths so it was just marked as 0. 
The highest cases in each state data frame contains a total number closer
to 50 because there is less of a chance for there to be a tie, since the
number of cases for every county must be greater than 0.  

## Reflection 5
What do you think about the number and scale of the inconsistencies in the data? Does the fact that there are inconsistencies mean that people should not use this data? Why or why not? Answer in at least 1-3 sentences

I think that the number and scale of inconsistencies in the total case and
death count for the counties data frame compared to the national data frame is misleading at first, but overall not too detrimental to this data's accuracy.
There is only a difference of 27 instances where the total counties case count
did not exactly match the case count for the overall US on that particular
date. If you observe the differences in the numbers, they are not too far
off. There are many acceptable reasons as to why this difference occurred,
such as human error or missed diagnosis or report of a case. All data sets
need room for error, and this data is a great example of including that,
but still being an excellent analysis of COVID tracking for the US. 

## Reflection 6
Why were you interested in this particular question? Were you able to answer your question with code? What did you learn? Answer in at least 1-3 sentences

I was interested in seeing the ratio in COVID-related deaths to cases in
King County because I know this county experienced a massive amount of cases,
but was unaware of the exact death count and how the ratio/death rate would
turn out to be. To answer this question I just filtered through the
"counties" dataset for the location of King County, Washington
(since there are counties in other states also called King) for the maximum
number of cases and placed those in two different variables. Then I just
divided the total deaths in King by the total cases in King to get the ratio,
which was fortunately low at around 0.6%. I learned that the total number of
deaths in King County was actually quite low at around 2,774 over the course
of 3 years, with over 400,000 cases, a number lower than what I was expecting
just based on King's large population (2 million).  

## Reflection 7
What, if anything, made you curious about this COVID analysis? What, if anything, surprised you? What might you do the same or differently on your next data wrangling project? Answer in at least 1-3 sentences

I was particularly curious about the data for the US counties and what it
meant to be an "Unknown". Not all of the "Unknown" counties had case/death
counts of zero, some had pretty significant numbers for being an
"Unknown" county which makes me think it may be a sort of geographical
barrier or unidentified area of the state where these reports were coming
from.I was surprised by the amount of informationthat was available
(and included) for U.S territories such as American Samoa, U.S Virgin Islands,
and Puerto Rico, as those places are often overlooked and not considered
states, so it was nice to see them included. I would probably find ways
to merge/consolidate data together in a way that would be the most
helpful for the purpoes of the project, for instance, most of this project
focused on the maximum values for the counties, states, etc. and
therefore only need the values taken from the most recent date. To make
things easier, I would probably filter out data that fit the specific time
frame (the tail of the data frame since the collection is cumulative) I was 
focusing on to prevent myself from having to filter out for the max
every time.  


