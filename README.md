# Identification of Types of Event-Time Temporal Relations in Portuguese Using a Rule-Based Approach

In this article, we present a computational method for identifying types of temporal relations between event and temporal expression in Portuguese texts. Employing a rule-based approach and sets of relevant features, we developed rulesets using rule learning algorithms, in addition to language-specific manual rules. Experiments on the TimeBankPT corpus[^timebankpt] demonstrated the effectiveness of our method, surpassing the baseline[^baseline] in terms of accuracy and F1-score. This research has practical applications in the fields of document summarization, story comprehension, and news analysis. By utilizing interpretable rules, it enables an enhanced understanding of time in texts.


# Feature Set
We present our [Feature Set](feature_set.md) organized by type of linguistic information.


# Rulesets
We present our [Rulesets](rules) developed for the task of identifying types of temporal relations between event and temporal expression in Portuguese texts.

Each rule follows the following format:

> *[rule code, 'TEMPORAL RELATION TYPE', rule order, "logical expression representing the rule", 'source algorithm', accuracy, total correct, number of times the rule was triggered]*

The logical expression representing the rule is composed of conjunctions of conditions. Each condition consists of a `feature` from our [feature set](feature_set.md), an `operator`, which can be equality or inequality, and the `value` of the feature.


# Final Results

We present the [final results](source/Final_Result_Rulesets.ipynb) of the experiments conducted on the training and testing data for all rulesets. The results take into account two distinct approaches for rule application: the first rule triggered and the voting system.


# References

[^timebankpt]: Francisco Costa and António Branco. 2012. TimeBankPT: A TimeML Annotated Corpus of Portuguese. In LREC, volume 12, pages 3727–3734. Available [here](http://nlx-server.di.fc.ul.pt/~fcosta/TimeBankPT/).
[^baseline]: Francisco Nuno Quintiliano Mendonça Carapeto Costa. 2012. Processing Temporal Information in Unstructured Documents. Ph.D. thesis, Universidade de Lisboa (Portugal).
