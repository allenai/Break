## **A Question Understanding Benchmark**

Break is a question understanding dataset of natural language questions annotated with their Question Decomposition Meaning Representations (QDMRs). It features [83,978](https://github.com/allenai/Break) human composed natural questions over text, images and datbases sampled from [10 leading question-answering benchmarks](#question-answering-datasets). Each example is annotated with strong supervision in the form of its question decompositions (QDMR).
Break was collected by a team of NLP [researchers](#authors) at [Tel Aviv University](https://www.tau-nlp.org/) and [Allen Institute for AI](https://allenai.org/).


For more details about Break, please refer to our [TACL 2020 paper](#paper).


## **Question-Answering Datasets**

The Break dataset contains questions from the following 10 datasets:  
* **Semantic Parsing**: [Academic](https://github.com/jkkummerfeld/text2sql-data), [ATIS](https://github.com/jkkummerfeld/text2sql-data), [GeoQuery](https://github.com/jkkummerfeld/text2sql-data), [Spider](https://yale-lily.github.io/spider)
* **Visual Question Answering**: [CLEVR-humans](https://cs.stanford.edu/people/jcjohns/clevr/), [NLVR2](http://lil.nlp.cornell.edu/nlvr/)
* **Reading Comprehension (and KB-QA)**: [ComQA](http://qa.mpi-inf.mpg.de/comqa/), [ComplexWebQuestions](https://www.tau-nlp.org/compwebq), [DROP](https://allennlp.org/drop), [HotpotQA](https://hotpotqa.github.io/)  

For the full dataset statistics please refer to our [repository](https://github.com/allenai/Break).


## **Paper**

[**Break It Down: A Question Understanding Benchmark**](https://arxiv.org/)  
Tomer Wolfson, Mor Geva, Ankit Gupta, Matt Gardner, Yoav Goldberg, Daniel Deutch and Jonathan Berant  
*Transactions of the Association for Computational Linguistics (TACL), 2020*  

```markdown
@article{Wolfson2020Break,
  title={Break It Down: A Question Understanding Benchmark},
  author={Wolfson, Tomer and Geva, Mor and Gupta, Ankit and Gardner, Matt and Goldberg, Yoav and Deutch, Daniel and Berant, Jonathan},
  journal={Transactions of the Association for Computational Linguistics},
  year={2020},
}
```

## **Authors**

> Talent wins games, but teamwork and intelligence wins championships.

*Michael Jordan*

<div>
<div class="card">
  <img src="images/authors/author_01.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="https://github.com/tomerwolgithub">
    <h4><b>Tomer Wolfson</b></h4>  
    </a>
  </div>
</div>
<div class="card">
  <img src="images/authors/author_02.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="https://mega002.github.io/">
    <h4><b>Mor <br>Geva</b></h4>  
    </a>
  </div>
</div>
<div class="card">
  <img src="images/authors/author_03.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="https://sites.google.com/view/ag1988/home">
    <h4><b>Ankit Gupta</b></h4>  
    </a>
  </div>
</div>
<div class="card">
  <img src="images/authors/author_04.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="https://allenai.org/team/mattg/">
    <h4><b>Matt Gardner</b></h4>  
    </a>
  </div>
</div>
<div class="card">
  <img src="images/authors/author_05.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="https://www.cs.bgu.ac.il/~yoavg/uni/">
    <h4><b>Yoav Goldberg</b></h4>  
    </a>
  </div>
</div>
<div class="card">
  <img src="images/authors/author_06.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="https://www.cs.tau.ac.il/~danielde/">
    <h4><b>Daniel Deutch</b></h4>  
    </a>
  </div>
</div>
<div class="card">
  <img src="images/authors/author_07.jpg" alt="Avatar" style="width:100%">
  <div class="container">
    <a href="http://www.cs.tau.ac.il/~joberant/">
    <h4><b>Jonathan Berant</b></h4>  
    </a>
  </div>
</div>
</div>


<div id="leaderboard"></div>
## **Leaderboard**

### **Submission**
An automatic submission to the [AI2 Leaderboard page](https://leaderboard.allenai.org/) will be avalable soon.

### **Results**

**QDMR Parsing**

Rank | Submission | Created | EM Dev. | EM Test
------------ | ------------- | ------------- | ------------- | -------------
1 | CopyNet *([Wolfson et al., TACL 2020](https://arxiv.org/))* | `Feb 1, 2020` | `15.40`  | `15.70`
2 | RuleBased *([Wolfson et al., TACL 2020](https://arxiv.org/))* | `Feb 1, 2020` | `00.20`  | `00.30` 


**High-level QDMR Parsing**

Rank | Submission | Created | EM Dev. | EM Test
------------ | ------------- | ------------- | ------------- | -------------
1 | CopyNet *([Wolfson et al., TACL 2020](https://arxiv.org/))* | `Feb 1, 2020` | `08.10`  | `08.30`
2 | RuleBased *([Wolfson et al., TACL 2020](https://arxiv.org/))* | `Feb 1, 2020` | `01.00`  | `01.20` 

<div id="explore"></div>
## **Explore**

<div>
  <p class="note">
     <i>83,978 question decompositions</i>
  </p>
  <p class="note">
    <i>59,823 QDMR logical forms</i>
  </p>
  <p class="note">
      <i>Questions from 10 question-answering datasets</i>
  </p>
  <p class="note">
      <i>Questions from 3 distinct modalities - text, images and database</i>
  </p>
</div>

- 83,978 question decompositions  
- 59,823 QDMR logical forms  
- Questions from 10 question-answering datasets  
- Questions from 3 distinct modalities - text, images and database  

- To learn more about Break [read our blogpost](/blogpost.md).  
- To view question decomposition examples [explore Break](/explore.md).

<img src="images/qdmr01.png" height="170">


<div id="dowload"></div>
## **Download**
Click here
