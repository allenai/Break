## Break: a New Dataset and Challenge for Question Understanding

- *Check out [our blogpost](https://medium.com/ai2-blog) at the official [AI2 blog!](https://medium.com/ai2-blog)*  

Increasing work has been devoted to models that can reason and integrate information from multiple parts of an input. This includes reasoning over images, paragraphs, documents, tables and more. *Question answering* (QA) is commonly used to probe these models ability to reason. In most QA tasks, a complex natural language question is posed, and is to be answered given a particular context (text, image, KB). While questions often share structure regardless of the particular task, understanding the language of complex questions has thus far been dealt within each task in isolation (reading comprehension, visual question answering, semantic parsing). For example, all of the questions in the figure below require operations such as fact chaining and counting. 
We propose *question understanding* as a standalone language understanding task. In particular, we focus on the decomposition of complex natural questions. This ability, to compose and decompose questions, lies at the heart of human language [1] and allows us to tackle previously unseen problems. Thus, better question understanding models should improve performance and generalization in tasks that require multi-step reasoning or that do not have access to substantial amounts of data. 


<a href="https://allenai.github.io/Break/images/qdmr01.png"> 
    <img src="images/qdmr_example.png" height="250">
 </a>

### Representing the Meaning of Questions
We introduce a formalism for representing the meaning of questions, and is agnostic to the information source. Our formalism, Question Decomposition Meaning Representation (QDMR), is inspired by database query languages and by semantic parsing, in which questions are given full meaning representations.
We express complex questions via simple questions ("operators") that can be executed in sequence to answer the original question. Each QDMR operator either selects a set of entities, retrieves information about their attributes, or aggregates information over entities. While this has been formalized in knowledge-base (KB) query languages, the same intuition can be applied to other modalities, such as images and text. QDMR abstracts away the context needed to answer the question, allowing in principle to query multiple sources for the same question.
In contrast to semantic parsing, QDMR is expressed through natural language phrases, facilitating annotation at scale by non-experts. 
Below we see to examples of questions along with their QDMR representations. Note that the references to previous decomposition steps enable us to represent QDMR as a directed-acyclic-graph.
For the full description of the QDMR formalism please refer to [our paper]().

<p float="left">
  <a href="https://allenai.github.io/Break/images/qdmr01.png"> 
    <img src="images/qdmr01.png" height="170">
  </a>
  <a href="https://allenai.github.io/Break/images/qdmr02.png"> 
    <img src="images/qdmr02.png" height="170">
  </a>
</p>


### The Data

QDMR serves as the formalism for creating Break, a question understanding dataset, aimed at probing question understanding models. It features 83,978 natural language questions, annotated with their Question Decomposition Meaning Representations (QDMRs). Break contains human composed questions, sampled from 10 leading question-answering benchmarks:
- Semantic Parsing: Academic, ATIS, GeoQuery, Spider
- Visual Question Answering: CLEVR-humans, NLVR2
- Reading Comprehension (and KB-QA): ComQA, ComplexWebQuestions, DROP, HotpotQA
Break was collected through crowdsourcing, with a user interface that allows us to train crowd workers to produce quality decompositions. Validating the quality of annotated structures reveals 97.4% to be correct.
Our paper ["Break It Down: A Question Understanding Benchmark"](), which has been accepted for publication in Transactions of the Association for Computational Linguistics, has a full description of the data collection process. To see some more examples from the dataset, please check out [the Break website](). For the full statistics on Break please refer to the [dataset repository]().

<a href="https://allenai.github.io/Break/images/qdmr01.png"> 
    <img src="images/break_question_modalities.png" height="200">
 </a>


### The *"Break It Down!"* Challenge

Break is aimed at enabling systems to effectively parse natural questions into their respective QDMR representations.
We hope that the release of Break, and its associated challenges, will help spur the development of question understanding models. We further encourage the NLP community to also treat Break as a resource for building better question answering systems. Our research has shown that multi-hop QA models utilizing Break decompositions greatly outperform a string baseline which does not. Additionally, we provide [neural QDMR parsing models](https://allenai.github.io/Break/#leaderboard), trained on Break, that beat a rule-based baseline that employs dependency parsing and coreference resolution.
Please visit the [Break website]() to view the leaderboard and learn more.


[1] Francis Jeffry Pelletier. 1994. The principle of semantic compositionality. Topoi, 13(1):11–24.
