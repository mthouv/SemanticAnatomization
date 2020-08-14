# Semantic anatomization

The goal of is this repo is to provide complementary information for our poster "Knowledge Graph Anonymization using Semantic Anatomization" submitted to ISWC 2020.


## Directory "queries"
It contains the different queries mentionned in the article:
* *query_inital_cluster* corresponds to the query referenced in section 4.3 allowing us to retrieve the initial clusters used in our algorithm
* *query_update* corresponds to the query referenced in section 4.5 allowing us to insert intermediary nodes between the EoIs and the SAs.

## Algorithm
Here we provide the pseudo-code for the algorithm described in section 2.

![](algo/algo.pdf)


## Religion ontology

This is the 4-level hierarchy we used to extend our LUBM datasets

![](onto/onto_religion.pdf)


## Evaluation

We provide the effectiveness results presented in the poster in section 3 as well as complementary results about queries involving 3 and 4 attributes. 
We also added the results for one of the suppression-based technique mentionned in the poster.
Finally, we present several tables summarizing the efficiency of our approach in regards to execution times.

### Effectiveness to anwser counting queries

Two attributes / One sensitive attribute

![](results/relative_error/rel_error_2_1.pdf)

Two attributes / Two sensitive attributes

![](results/relative_error/rel_error_2_2.pdf)

Three attributes / One sensitive attribute

![](results/relative_error/rel_error_3_1.pdf)

Three attributes / Two sensitive attributes

![](results/relative_error/rel_error_3_2.pdf)

Four attributes / One sensitive attribute

![](results/relative_error/rel_error_4_1.pdf)

Four attributes / Two sensitive attributes

![](results/relative_error/rel_error_4_2.pdf)


### Comparison with a suppression technique: Query-based linked data anonymization by Delanaux et al.

2 attributes / One sensitive attribute

![](results/delanaux_relative_error/eval_delanaux_2_1.pdf)

3 attributes / Two sensitive attributes

![](results/delanaux_relative_error/eval_delanaux_3_1.pdf)


In a generalization/suppression context, we can only assume a uniform distribution for the values of the sensitives attributes. Hence, in the above-figures, we can see that the technique performs well when the values are indeed uniformly distributed but fails to provide satisfiable results otherwise.

### Efficiency

The tables summarize the execution times of the various steps of the algorithm. We present the results for our *hasReligion* predicate (Table 1) but we also experimented with other predicates from the LUBM ontology, namely *publicationAuthor* (Table 2) and *advisor* (Table 3).


![](results/efficiency/efficiency_religion.pdf)


![](results/efficiency/efficiency_publicationAuthor.pdf)


![](results/efficiency/efficiency_advisor.pdf)


Since our approach is primarily dependent on the number of distinct values for the SA rather than the size of the graph, we observe constant and relatively low execution times for the *hasReligion* predicate.

On the other hand, tho objects for the *publicationAuthor* and *advisor* being professor nodes, the number of distinct values for both predicates grows with the size of the graph so the execution times grow as well.