# Break: A Question Understanding Benchmark

<img align="left" src="images/break.svg" height="100"></img>
Break is a human annotated dataset of natural language questions and their Question Decomposition Meaning Representations (QDMRs). Break consists of 83,978 examples sampled from 10 question answering datasets over text, images and databases.
This repository contains the Break dataset along with information on the exact data format.

For more details check out our TACL paper ["Break It Down: A Question Understanding Benchmark"](https://arxiv.org/abs/2001.11770v1), and [website](https://allenai.github.io/Break/).  
The code and models presented in our [paper](https://arxiv.org/abs/2001.11770v1), see our repository at: [https://github.com/tomerwolgithub/Break](https://github.com/tomerwolgithub/Break).



* **Key Links**
	* **Break Dataset**: [Download](https://github.com/allenai/Break/raw/master/break_dataset/Break-dataset.zip)
	* **Paper**: ["Break It Down: A Question Understanding Benchmark"
](https://arxiv.org/abs/2001.11770v1)
	* **Models Code**: [https://github.com/tomerwolgithub/Break](https://github.com/tomerwolgithub/Break)
	* **Leaderboard**:  
		* Break:  [Leaderboard](https://leaderboard.allenai.org/break/)
		* Break High-Level:  [Leaderboard](https://leaderboard.allenai.org/break_high_level/)
		* Evaluator Code: [https://github.com/allenai/break-evaluator](https://github.com/allenai/break-evaluator)
	* **Website**: [https://allenai.github.io/Break/](https://allenai.github.io/Break/)
	* **Huggingface `nlp` library**: [https://huggingface.co/datasets/break_data](https://huggingface.co/datasets/break_data)


### Changelog
- `7/04/2020` Break is now part of [HuggingFace `nlp` library](https://huggingface.co/datasets/break_data) see [details](#HuggingFace-nlp-library).
- `4/10/2020` Pretrained QDMR Parsing models are now [available](https://github.com/tomerwolgithub/Break/tree/master/qdmr_parsing#cofiguration-and-petrained-models).
- `4/02/2020` New AI2 leaderboards for [Break](https://leaderboard.allenai.org/break/) and [Break High-Level](https://leaderboard.allenai.org/break_high_level/).
- `2/26/2020` Our paper's entire codebase is now [available](https://github.com/tomerwolgithub/Break).
- `1/31/2020` The entire codebase and official leaderboard will be released soon.
- `1/31/2020` The full Break dataset has been released!

## Question Answering Datasets

* The Break dataset contains questions from the following 10 datasets: 
	* **Semantic Parsing**: [Academic](https://github.com/jkkummerfeld/text2sql-data), [ATIS](https://github.com/jkkummerfeld/text2sql-data), [GeoQuery](https://github.com/jkkummerfeld/text2sql-data), [Spider](https://yale-lily.github.io/spider)
	* **Visual Question Answering**: [CLEVR-humans](https://cs.stanford.edu/people/jcjohns/clevr/), [NLVR2](http://lil.nlp.cornell.edu/nlvr/)
	* **Reading Comprehension (and KB-QA)**: [ComQA](http://qa.mpi-inf.mpg.de/comqa/), [ComplexWebQuestions](https://www.tau-nlp.org/compwebq), [DROP](https://allennlp.org/drop), [HotpotQA](https://hotpotqa.github.io/)

## Data Description

### Datasets


* [**``QDMR``**](https://github.com/allenai/Break/tree/master/break_dataset/QDMR): Contains questions over text, images and databases annotated with their Question Decomposition Meaning Representation. In addition to the train, dev and (hidden) test sets we provide ``lexicon_tokens`` files. For each question, the lexicon file contains the set of valid tokens that could *potentially* appear in its decomposition ([Section 3](https://arxiv.org/abs/2001.11770v1)).
* [**``QDMR high-level``**](https://github.com/allenai/Break/tree/master/break_dataset/QDMR-high-level): Contains questions annotated with the *high-level* variant of QDMR. These decomposition are exclusive to Reading Comprehension tasks ([Section 2](https://arxiv.org/abs/2001.11770v1)). ``lexicon_tokens`` files are also provided. 
* [**``logical-forms``**](https://github.com/allenai/Break/tree/master/break_dataset/logical-forms): Contains questions and QDMRs annotated with full logical-forms of QDMR operators + arguments. Full logical-forms were inferred by the annotation-consistency algorithm described in [Section 4.3](https://arxiv.org/abs/2001.11770v1).


### Data Format

* QDMR & QDMR high-level:
	* train.csv, dev.csv, test.csv:
		* **``question_id``**: The Break question id, of the format ``[ORIGINAL DATASET]_[original split]_[original id]``. E.g., ``NLVR2_dev_dev-1049-1-1`` is from NLVR2 dev split with its NLVR2 id being, ``dev-1049-1-1``.
		* **``question_text``**: Original question text.
		* **``decomposition``**: The annotated QDMR of the question, its steps delimited by ``;``. E.g., ``return flights ;return #1 from  washington ;return #2 to boston ;return #3 in the afternoon``.
		* **``operators``**: List of tagged QDMR operators for each step. QDMR operators are fully described in ([Section 2](https://arxiv.org/abs/2001.11770v1)) of the paper. The 14 potential operators are, ``select, project, filter, aggregate, group, superlative, comparative, union, intersection, discard, sort, boolean, arithmetic, comparison``. Unidefntified operators are tagged with ``None``.
		* **``split``**: The Break dataset split of the example, train / dev / test.
	* train_lexicon_tokens.json, dev_lexicon_tokens.json, test_lexicon_tokens.json:
		* **``"source"``**: The source question.
		* **``"allowed_tokens"``**: The set of valid lexicon tokens that can appear in the QDMR of the question. For the method used to generate lexicon tokens see [here](https://github.com/tomerwolgithub/Break/blob/master/qdmr_parsing/README.md#lexicon-file-generation).
* logical-forms:
	* train.csv, dev.csv, test.csv:
		* **``question_id``**: Same as before.
		* **``question_text``**: Same as before.
		* **``decomposition``**: Same as before.
		* **``program``**: List of QDMR operators and arguments that the original QDMR was mapped to. E.g., for the QDMR, ``return citations ;return #1 of Making database systems usable ;return number of  #2``, its program is, ``[ SELECT['citations'], FILTER['#1', 'of Making database systems usable'], AGGREGATE['count', '#2'] ]``.
		* **``operators``**: Same as before.
		* **``split``**: Same as before.

### Data Statistics

Break question decomposition datasets:

| Data | Examples | Train | Dev | Test |
|-----------|-------------------------|-------------------------|-------------------------|-------------------------|
| QDMR     | 60,150                   |       44,321 (73.7%)          |      7,760 (12.9%)           |      8,069 (13.4%)           |
| QDMR High-level | 23,828                   |     17,503 (73.5%)             |      3,130 (13.1%)           |        3,195 (13.4%)         |
| logical-forms (QDMR)    | 59,823                   |    44,098 (73.7%)             |    7,719 (12.9%)             |   8,006 (13.4%)              |


QDMR annotations by original dataset:  

| Data | Examples | Train | Dev | Test |
|-----------|-------------------------|-------------------------|-------------------------|-------------------------|
| [Academic](https://github.com/jkkummerfeld/text2sql-data)     | 195                   |  195                |       0           |   0               |
| [ATIS](https://github.com/jkkummerfeld/text2sql-data)     | 4,906                   |  4,042                |   457               |  407                |
| [GeoQuery](https://github.com/jkkummerfeld/text2sql-data)     | 877                   |   547               |    50              | 280                 |
| [Spider](https://yale-lily.github.io/spider)     | 7,982                   |   6,955               |    502              |   525               |
| [CLEVR-humans](https://cs.stanford.edu/people/jcjohns/clevr/)     | 13,935                   |      9,453            |    2,215              |     2,267             |
| [NLVR2](http://lil.nlp.cornell.edu/nlvr/)     | 13,517                   |     9,915             |   1,805               |    1,797              |
| [ComQA](http://qa.mpi-inf.mpg.de/comqa/)     | 5,520                   |    3,546              |    988              |     986             |
| [ComplexWebQuestions](https://www.tau-nlp.org/compwebq)     | 2,988                   |     1,985             |     475             |       528           |
| [DROP](https://allennlp.org/drop)     | 10,230                  |    7,683              |   1,268               |     1,279             |


QDMR *High-level* annotations by original dataset:  


| Data | Examples | Train | Dev | Test |
|-----------|-------------------------|-------------------------|-------------------------|-------------------------|
| [ComplexWebQuestions](https://www.tau-nlp.org/compwebq)     | 2,991                   |     1,988             |     475             |        528          |
| [DROP](https://allennlp.org/drop)     | 10,262                   |     7,705             |      1,273            |     1,284             |
| [HotpotQA-hard](https://hotpotqa.github.io/)     | 10,575                   |     7,810             |     1,382             |    1,383              |

## Reference

```
@article{Wolfson2020Break,
  title={Break It Down: A Question Understanding Benchmark},
  author={Wolfson, Tomer and Geva, Mor and Gupta, Ankit and Gardner, Matt and Goldberg, Yoav and Deutch, Daniel and Berant, Jonathan},
  journal={Transactions of the Association for Computational Linguistics},
  year={2020},
}
```

## HuggingFace nlp library

You can also access Break as part of the  [HuggingFace `nlp` library](https://github.com/huggingface/nlp):

```python
!pip install nlp
from nlp import load_dataset
dataset = load_dataset('break_data', 'QDMR-high-level')
# dataset = load_dataset('break_data', 'QDMR')
```
Break is referenced [here](https://huggingface.co/datasets/break_data) and can be [browsed online](https://huggingface.co/nlp/viewer/?dataset=break_data) as part of a simple viewer.  
More details on the options and usage for this library can be found on the `nlp` repository at [https://github.com/huggingface/nlp](https://github.com/huggingface/nlp).
