# ELSA - a Norwegian Entity-level sentiment dataset

The enclosed files contain our Entilty-level annotations of the [Norec_fine](https://github.com/ltgoslo/norec_fine) dataset. Our annotations provide separate annotations for each volitional entity in each document. The Norec_fine texts are drawn from [NoReC](https://github.com/ltgoslo/norec). The NoReC repo contains metadata about the texts in our dataset, e.g. category, date of publishing, and author(s).  

**The paper** presenting this dataset [can be found here](http://arxiv.org/abs/2407.03916).

## Folder [annotations](annotations)
### doc_data
This export contains the different texts with their reference ID back to NoReC, a list of the volitional entity IDs found in the text, the document text. split into sentences, the character-level sentence boundaries, and the train-dev-test where this document belongs, according to Norec_fine. `'norec_id', 'elsa_ids', 'sentence_texts', 'sentence_boundaries', 'split'`.  
This information is used by the other exports, to retrieve the document text, and each sentence separately, accessed by the `'sentence_texts'` list indices.

### elsa_overall
This exports contain one entry per volitional entity and presents the annotators' evaluation of the overall sentiment that this text conveys regarding the given entity. `'norec_id', 'elsa_id', 'split', 'text', 'elsa_overall_sentiment'`

### elsa_sentences
This export contains the aggregated sentiment in each sentence regarding the given volitional entity. Sentences with no sentiment annotation are regarded "Neutral" `'norec_id', 'elsa_id', 'split', 'sentence_idx', 'sentencelevel_agg'`

### elsa_lowlevel
This export contains each sentiment annotation in the dataset, apart from the overall sentiment presented in `elsa_overall`.  
The annotations here is the basis for the aggregations presented in `elsa_sentences`. Each reference category is available for analysis, and one may wish to aggregate this information according to a different heuristics.  
 `'reference_cat', 'sentiment', 'begin', 'end', 'text', sentence_idx', 'norec_id', 'elsa_id', 'split'`

## Folder [LAW-XVIII_2024](LAW-XVIII_2024)
Contains data especially related to [our paper](LAW-XVIII_2024/EACL_LAW.pdf) at the LAW-XVIII 2024 workshop.
