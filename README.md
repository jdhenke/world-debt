This interface shows two matrices of world debt statistics according to [this report](http://www.bis.org/statistics/provbstats.pdf#page=7) in 2011.

1. The first is the raw data of who owes who.
2. The second also shows who owes who but with any cycles of debt removed.

A length two cycle would be A owes B and B owes A.
Rather than both of them owing eachother, the larget debtor should just owe the difference to the smaller one.

More generally, it finds all cycles and reduces the weight of all edges in the cycle by the minimum edge weight in the cycle.
The minimum weight edge then has a weight of 0, so it is then removed, removing the cycle.
This results in a graph showing debts where no country owes itself by transitivity.

Show total of cumulative debt.
