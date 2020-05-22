# Semantic anatomization

The goal of is this repo is to provide complementary information for our paper "Knowledge Graph Anonymization using Semantic Anatomization" submitted to ISWC 2020.

It is organized in several directories.


## Directory "queries"
It contains the different queries mentionned in the article:
* *query_inital_cluster* corresponds to the query referenced in section 4.3 allowing us to retrieve the initial clusters used in our algorithm
* *query_update* corresponds to the query referenced in section 4.5 allowing us to insert intermediary nodes between the EoIs and the SAs.

## Directory "results"

It contains the results presented in the paper in section 6. The files are named as follows "*\*_i_j.pdf*"" where *i* corresponds to the number of attributes involved in the query and *j* corresponds to the number of SA among the *i* attributes. 

A "*\*_summary.pdf*" file is also provided in each sub-directory and presents the data that were used to produce the graphs in tabular form.
* Directory "relative_error" corresponds to Figure 4
* Directory "absolute_mean_error" corresponds to Figure 5
* Directory "delanaux_relative_error" corresponds to Figure 6