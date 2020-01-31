# Break: A Question Understanding Benchmark

<img align="left" src="images/hammer_and_anvil-1.png" height="100"></img>
Break is a human annotated dataset of natural language questions and their Question Decomposition Meaning Representations (QDMRs). Break consists of 83,978 examples sampled from 10 question answering datasets over text, images and databases.
This repository contains the Break dataset along with information on the exact data format.

For more details check out our TACL paper ["Break It Down: A Question Understanding Benchmark"](https://arxiv.org/), and [website](https://allenai.github.io/Break/).  
The code and models presented in our [paper](https://arxiv.org/), see our repository at: [https://github.com/tomerwolgithub/Break](https://github.com/tomerwolgithub/Break).



* **Key Links**
	* **Break Dataset**: [https://github.com/allenai/Break/tree/master/break_dataset](https://github.com/allenai/Break/tree/master/break_dataset)
	* **Paper**: ["Break It Down: A Question Understanding Benchmark"
](https://arxiv.org/)
	* **Paper Code**: [https://github.com/tomerwolgithub/Break](https://github.com/tomerwolgithub/Break)
	* **Leaderboard**:  [Coming Soon](https://leaderboard.allenai.org/)
	* **Website**: [https://allenai.github.io/Break/](https://allenai.github.io/Break/)


### Changelog

- `1/31/2020` The full dataset, has been added.

## Question Answering Datasets

* The Break dataset contains questions from the following 10 datasets: 
	* **Semantic Parsing**: [Academic](https://github.com/jkkummerfeld/text2sql-data), [ATIS](https://github.com/jkkummerfeld/text2sql-data), [GeoQuery](https://github.com/jkkummerfeld/text2sql-data), [Spider](https://yale-lily.github.io/spider)
	* **Visual Question Answering**: [CLEVR-humans](https://cs.stanford.edu/people/jcjohns/clevr/), [NLVR2](http://lil.nlp.cornell.edu/nlvr/)
	* **Reading Comprehension (and KB-QA)**: [ComQA](http://qa.mpi-inf.mpg.de/comqa/), [ComplexWebQuestions](https://www.tau-nlp.org/compwebq), [DROP](https://allennlp.org/drop), [HotpotQA](https://hotpotqa.github.io/)

## Data Description

### Datasets


* [**``QDMR``**](https://github.com/allenai/Break/tree/master/break_dataset/QDMR):
* [**``QDMR high-level``**](https://github.com/allenai/Break/tree/master/break_dataset/QDMR-high-level):
* [**``logical-forms``**](https://github.com/allenai/Break/tree/master/break_dataset/logical-forms):


### Data Format

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

