# Project 1: Standardized Test Analysis
-By Zach Fuller

---
## Problem Statement

Standardized testing has been a debated, modified, and still used system for grading the projected ability of a high school student's success in the next level(s) of academia. While this can be controversial and problematic for college and university admission staffs, the core of such a standardized test has been and will continue to be used. Let's look at participation rates as a measure of success for SAT scores.

---
## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT by year|The state locaton for the corresponding data|
|participation|float|SAT by year|The participation rate by state for students taking the SAT by year|
|read_write|integer|SAT by year|The Evidence-Based Reading and Writing portion of the SAT score by year, where the range is 200 to 800|
|math|integer|SAT by year|The Math portion of the SAT score by year, where the range is 200 to 800|
|total|integer|SAT by year|The total SAT score by year, where the range is 400 to 1600|

---
## Datasets

* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))

---
## Analysis

### Participation Analysis:
For participation rate by state, we see an increase in the number of states meeting 100% participation year over year (2017:4, 2018:5, 2019:8). Conversely, we also see a decrease in the number of states with under 5% participation year over year (2017:14, 2018:13, 2019:12). This would show that the changes made to the test in 2016 did encourage turnout to take the SAT. Let's loosen the limits and look at the states by greater than or equal to 90%. We also see a year over year growth from 7 states in 2017 to 10 states in 2018 and 12 states in 2019. Let's also look at states less than or equal to 10%. We also see a year over year growth from 19 states in 2017 to 18 states in 2018 and 17 states in 2019.

It is noted that the participation bracket of < 10% shows 17 states from 2017-2019, as well as the bracket > 90% showing 12 states from 2017-2019, and finally the bracket in the middle showing 22 states from 2017-2019.

### Highest Score Analysis:
We see very quickly that the states with the highest scores also have the lowest participation rate which shows that only the best test takers are taking the SAT. If we look at highest SAT score by states with 100% participation, we also see a different skewed result. Instead, we see almost the worst SAT scores by state.

If we only look at states that have a participation rate greater than 20%, we see a better picture of which states produce the best test takers. The filtered data set directly above shows this, and we can see that Massachusetts has the highest SAT score for the largest participation rate.

## Lowest Score Analysis:
When we look at the bottom 5 SAT scores by state we also see a different picture. The majority of the bottom 5 and bottom 10 did have a high participation rate. This shows that a heavy involvement in participation is most likely to yield lower results as all levels of test taking skills are included. The most concerning results are states in the bottom 10 that have a low participation rate. This would show that not many students participated and the ones that did tested poorly. In 2017, Oklahoma was under 10% and ranked 9th lowest. In 2018, Utah was at 4% and ranked 5th lowest. In 2019, Oklahoma improved to 22% participation but ranked 2nd lowest.

---
## Conclusions and Recommendations

Participation rate paints a very clear picture of where your state may be relative to the nation as a whole. States with the lowest participation rates (below 10%) produced the highest scores. This is to say these states produce some of the highest overachievers in the country. They were not required to take the test, but they did and excelled. All test scores for the states shown below are above the 75th percentile.

**Overachieving Top 5** 

**2017**
> 1. Minnesota
> 2. Wisconsin
> 3. Iowa
> 4. Missouri
> 5. Kansas

**2018**
> 1. Minnesota
> 2. Wisconsin
> 3. North Dakota
> 4. Iowa
> 5. Kansas

**2019**
> 1. Minnesota
> 2. Wisconsin
> 3. South Dakota
> 4. North Dakota
> 5. Nebraska

We can also note which states produced the highest test scores when requiring SAT to be taken by high school students. This group also shows some consistency from year to year. However, all of these test scores are below the 25th percentile. This would show that school districts in these states need to focus on test preparation for a test that they deemed manditory.

**100% Participation Top 5** 

**2017**
> 1. Connecticut
> 2. Michigan
> 3. Delaware
> 4. Washington DC

**2018**
> 1. Connecticut
> 2. Colorado
> 3. Michigan
> 4. Idaho
> 5. Delaware

**2019**
> 1. Connecticut
> 2. Colorado
> 3. Illinois
> 4. Michigan
> 5. Florida

Lastly, let's take note of states that produced the highest SAT scores without reaching 100% participation. These states all produced scores above the 50th percentile and slightly above and below the nation average.

**Best of the Rest Top 5** 

**2017**
> 1. Arizona
> 2. Nevada
> 3. Vermont
> 4. Oregon
> 5. Massachusetts

**2018**
> 1. Arizona
> 2. Nevada
> 3. Massachusetts
> 4. Vermont
> 5. Virginia

**2019**
> 1. Nevada
> 2. Arizona
> 3. Massachusetts
> 4. Virginia
> 5. Oregon

A high SAT score does provide a glimpse at a student's appitude for being able to quickly and accurately answer questions. These are valuable skills to have. It is on the individual state's composite school boards to ensure the resources are available to encourage students to prepare and excell for these tests.
