# Project Proposal
## Group Members
Derek Situ, Jin Manabe, Jin Wang, Laura Bruno-Johansen, Mea Srisan

## Summary
In powerlifting competitions, competitors have three attempts to perform each of the three lifts (squat, bench press, deadlift), for a total of nine attempts. The sum of a competitor’s greatest (in terms of amount of weight lifted) successful attempts for each of the three lifts is called their “total”, and rankings within each weight class are decided by the totals submitted by competitors. At the highest levels of competition, strategic interactions in the ninth round are often the deciding factors in determining winners and losers. This is because after the eighth round, all competitors know their subtotal, as well as their opponents’ subtotals. At this stage they also tend to formulate beliefs about one another’s eventual totals, since they only need to account for one last attempt that could influence each lifter’s total. We plan to model these last-attempt selections and evaluate how well our model fits real competition data. In reality, a player’s payoffs could be influenced by many factors, but it may be reasonable to assume that the following items make up an exhaustive list of factors for the purposes of our model (we may even want to simplify it further):

* Their ranking
* Their “IPF Points”, which is a function of the player’s total, bodyweight, and sex
* Breaking records
* Their team’s ranking and IPF points

We will draw our data from https://www.openpowerlifting.org/, which hosts a continually updated database containing competition results for almost every sanctioned (official) powerlifting meet in the world. From this database we plan to model and analyze World Classic Powerlifting Championships hosted by the International Powerlifting Federation from 2012 to 2021. We will limit ourselves to competitions from one federation so that we do not have to consider varying rules across federations, and we only consider world championship-level competitions since competitors are more likely to act rationally at this level, and our assumptions about a competitor’s payoffs are more likely to be accurate. For example, a competitor at a local or provincial level competition may only care about breaking personal records, or successfully submitting their first total in a competition setting. They may also not be sufficiently familiar with the rules so as to make optimal strategic attempt selections.

Concepts in game theory that we can apply include:

* Uncertainty over the success of a lift
* Asymmetric information
  * A lifter’s belief about their eventual total tends to be more accurate than another
lifter’s beliefs about the same total
  * e.g. for a total $T$ and lifters $\{i, -i\}$, 
  $E[T_i - E_i[T_i]] < E[T_i - E_{-i}[T_i]]$
