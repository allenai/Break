# Break: A Question Understanding Benchmark

<img align="left" src="images/hammer_and_anvil-1.png" height="100"></img>
Break is a human annotated dataset of natural language questions and their Question Decomposition Meaning Representations (QDMRs). Break consists of 83,978 examples sampled from 10 question answering datasets over text, images and databases.
This repository contains the Break dataset along with information on the exact data format.

For more details check out our TACL paper ["Break It Down: A Question Understanding Benchmark"](https://arxiv.org/), and [website](https://allenai.github.io/Break/).



* **Key Links**
	* **Break Dataset**: [https://github.com/allenai/Break/tree/master/break_dataset](https://github.com/allenai/Break/tree/master/break_dataset)
	* **Paper**: ["Break It Down: A Question Understanding Benchmark"
](https://arxiv.org/)
	* **Leaderboard**:  [Coming Soon](https://leaderboard.allenai.org/)
	* **Website**: [https://allenai.github.io/Break/](https://allenai.github.io/Break/)


### Changelog

- `1/14/2020` The full dataset, models and entire codebase will be officially released following final paper acceptance.

## Question Answering Datasets

* The Break dataset contains questions from the following 10 datasets: 
	* **Semantic Parsing**: [Academic](https://github.com/jkkummerfeld/text2sql-data), [ATIS](https://github.com/jkkummerfeld/text2sql-data), [GeoQuery](https://github.com/jkkummerfeld/text2sql-data), [Spider](https://yale-lily.github.io/spider)
	* **Visual Question Answering**: [CLEVR-humans](https://cs.stanford.edu/people/jcjohns/clevr/), [NLVR2](http://lil.nlp.cornell.edu/nlvr/)
	* **Reading Comprehension (and KB-QA)**: [ComQA](http://qa.mpi-inf.mpg.de/comqa/), [ComplexWebQuestions](https://www.tau-nlp.org/compwebq), [DROP](https://allennlp.org/drop), [HotpotQA](https://hotpotqa.github.io/)

## The Break Dataset

## Reference

```
@inproceedings{break2020tacl,
  title={{Break It Down: A Question Understanding Benchmark}},
  author={Wolfson, Tomer and Geva, Mor and Gupta, Ankit and Gardner, Matt and Goldberg, Yoav and Deutch, Daniel and Berant, Jonathan},
  booktitle={Transactions of the Association for Computational Linguistics ({TACL})},
  year={2020}
}
```

