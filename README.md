# MBR ( Market Basket Analysis )
Market basket analysis explains the combinations of products that frequently co-occur in transactions. For example, people who buy bread and eggs, also tend to buy butter as many of them are planning to make an omelette. Marketing team should target customers who buy bread and eggs with offers on butter, to encourage them to spend more on their shopping basket.
<b>It is also known as "Affinity Analysis" or "Association Rule Mining".</b>
</br></br>
Association mining is usually done on transactions data from a retail market or from an online e-commerce store. Since most transactions data is large, the apriori algorithm makes it easier to find these patterns or rules quickly.
</br></br>
So, What is a rule?
</br>
A rule is a notation that represents which item/s is frequently bought with what item/s. It has an LHS and an RHS part and can be represented as follows:
</br></br>
itemset A => itemset B
</br></br>
This means, the item/s on the right were frequently purchased along with items on the left.
</br>
How to measure the strength of a rule?
</br>
The apriori() generates the most relevent set of rules from a given transaction data. It also shows the support, confidence and lift of those rules. These three measure can be used to decide the relative strength of the rules. So what do these terms mean?
</br>
Lets consider the rule A => B in order to compute these metrics.
![mbarule](https://github.com/shingareshubham/MBR/blob/master/mbarule.png)

</br>
Lift is the factor by which, the co-occurence of A and B exceeds the expected probability of A and B co-occuring, had they been independent. So, higher the lift, higher the chance of A and B occurring together.
</br>
Lets see how to get the rules, confidence, lift etc using the arules package in R.

# Example
<br>Transactions data
<br>Lets play with the Groceries data that comes with the arules pkg. Unlike dataframe, using head(Groceries)
