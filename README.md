
# 'Mental-Health in Tech' USA 2014 Survey Results 

## Project Background

Open Sourcing Mental Illness (OSMI) was a project initiated in 2013 by Open Sourcing Mental Health- a non-profit corporation dedicated to raising awareness, educating, and providing resources to support mental wellness in the tech and open source communities.

The organisation conducted the OSMI survey in 2014 to measure attitudes towards mental health in the tech workplace, and to examine the frequency of mental health disorders among tech workers. It received 1200+ responses from tech employees across 44 US States, on a staggering 26 dimensions, ranging from family history of mental illness to whether people felt comfortable talking about mental health with their colleagues, or their bosses. 

Know more about the survey through the Founder's Ted Talk here.


## Analysis Overview
From the survey dataset (OSMI_survey_2014.csv), this analysis provides answers to the following key questions:

1) Is there a significant gap in mental-health benefits provided by MSMEs and Large Enterprises? If yes, how wide?

2) Does a perception of total anonymity when taking advantage of mental health resources help in seeking treatment? 

3) If anonymity helps, is it from a fear of consequences when one discusses a mental health issue with their employer?

4) How comfortable are employees speaking about mental heatlh issues with their coworkers and with their immediate supervisors? (surprising answer)

5) How comfortable are people bringing up mental health issues with a potential employer in a job interview?

The Python script utilized to clean, analyse and visualise the data to answer the above questions can be found here.

## Executive Summary

The analysis was performed on a refined dataset of 883 tech-sector employee responses to the 2014 survey. By cross-referencing company size with individual psychological safety, it is observed that mental health support in tech is not just a resource issue, but also a cultural and transparency issue. Here are the key findings summarised:

* `The Enterprise Gap:` Large corporations (1000+ employees) are over 3.3x more likely to provide mental-health benefits than small startups (6-25 employees).

* `The Privacy Benefit:` Guaranteed anonymity increases treatment-seeking by 12% among at-risk employees.

* `The Stigma Effect:` Employees are 16x more comfortable discussing physical ailments than mental health.  

* `The Trust Hierarchy:` Employees trust their direct supervisors (40%) significantly more than their peers (18%).

* `The Interview Barrier:` While ~40% might talk to a current boss, only ~2% of candidates feel comfortable bringing up mental health in a future job interview.

## Data Integrity and Initial Checks

Before cleaning, the row count was- 1259 rows

a) Age issue- There were absurd entries in the age column- negative age (e.g. -78), or age higher than 120 years (e.g. 99999). To keep the analysis representative of the adult workforce, we only included entries with age greater than 18 and less than 75, while replacing all other entries with NaN.

b) Gender issue- Entries for gender had spelling errors and formatting discrepancies ('M', 'cis man', 'f', 'Femail', 'femake'). All were taken into account and classified into 'male', 'female' and 'other' using arrays.

c) Null values- In the work-interfere column, 264 null entries were noticed. They were replaced with 'Unknown' to record the number of people too uncomfortable to answer.

d) Relevant conditions- Considering the survey was done for employees within tech companies, all entries of self-employed people and people in non-tech companies were filtered out.

After cleaning and formatting, the row count was- 883 rows

## Key Methods and Findings 

Here are the key findings elaborated upon with appropriate visualisations.

1. The Startup Benefit Void-

There is a linear correlation between company size and benefit provision. In startups (1-25 employees), "No" is the most common answer regarding benefits, while in Large Enterprise, "Yes" dominates. However, "Don't Know" remains high across all sizes, suggesting a massive internal communication failure.

2. Anonymity as a Conversion Tool- 

When we filtered for employees whose mental health interferes with work, we found that 65.87% sought treatment when anonymity was protected, compared to only 54.17% when it was not. This strongly suggests that privacy is the primary gateway to care.

3. The Physical vs. Mental Stigma-

The "Stigma Effect" is stark. While 75% of employees believe discussing physical health has no negative consequences at work, only 40% feel the same about mental health. Mental health is still viewed as a professional liability.

4. The Peer Trust Gap-

Contrary to intuition, the manager isn't the primary barrier—the coworker is. Employees are more than 2x as likely to be comfortable talking to their supervisor than all their peers, indicating a fear of social judgment or professional competition among equals.

5. Present to Future Trust-

The present trust in one's current employer (found in #4) does not easily translate to trust in a future employer. We can see that only 2% of respondents will bring up a mental health issue in a future job interview. 

## Recommendations
