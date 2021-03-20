# Electon-Analysis
## Purpose
The prupose of this analysis is to summarize the [raw voting data](https://github.com/sd2wiebe/Electon-Analysis/tree/main/Resources) in order to determine who won the election, as well as other noteworthy data points, such as total votes cast etc.

## Results
### Total Votes
- There were 369,711 votes cast in this election
### By County
- Jefferson county had 10.51% (38,855)
- Denver county had 82.78% (306,055)
- Arapahoe county had 6.71% (24,801)

Denver County had the largest amount of votes with 306,055.
### By candidate:
- Charles Casper Stockham: 23.0% (85,213)
- Diana DeGette: 73.8% (272,892)
- Raymon Anthony Doane: 3.1% (11,606)
### Winner Summary
- Winner: Diana DeGette
- Winning Vote Count: 272,892
- Winning Percentage: 73.8%

## Election Audit Summary
This summary of voting data can be collected for any election using my code, barring some minor changes which I will address below.
The first thing that will have to be looked at is what columns of the raw data display the candidates name for each vote. The dataset used for this analysis displayed the candidate name for each vote on the third column/comma seperated value or each row:
<p align="center"

![alttext](https://github.com/sd2wiebe/Electon-Analysis/blob/main/Resources/columns.png)

</p>

Python indexing starts at 0, so the third value is referenced by ```[2]```
So for our analysis, to collect the candidate names we used:
```candidate_name = row[2]```
In order to alter this to fit a different data set, we simply need to replace ```[2]``` with the correct index corresponding to the candidate name.
Similarly, we need to change the index for ```County_name = row[1]``` to index the correct column in the new dataset that represents the name of the County/State etc.

