## Explore Break

Below you will find examples of questions and their QDMRs found in Break.   
Note that *high-level* QDMRs are less coarse in their decomposition, as they are geared towards reading comprehension tasks. For more details on *high-level* QDMRs please refer to [our paper](https://allenai.github.io/Break/#paper).

* **Semantic Parsing**: 
  * [Academic](#academic)
  * [ATIS](#atis)
  * [GeoQuery](#geoquery)
  * [Spider](#spider)
* **Visual Question Answering**: 
  * [CLEVR-humans](https://cs.stanford.edu/people/jcjohns/clevr/)
  * [NLVR2](http://lil.nlp.cornell.edu/nlvr/)
* **Reading Comprehension (and KB-QA)**: 
  * [ComQA](http://qa.mpi-inf.mpg.de/comqa/)
  * [ComplexWebQuestions](https://www.tau-nlp.org/compwebq)
  * [DROP](https://allennlp.org/drop)
  * [HotpotQA](https://hotpotqa.github.io/)  

### Academic

### ATIS

### GeoQuery

### Spider 

## CLEVR-humans

### NLVR2

### ComQA

### ComplexWebQuestions

### DROP

### HotpotQA

<div>
  <p class="note">
     <i>"Some question"</i>
  </p>
</div>
<div>
  <p class="note">
    <i>"A totally different and complex question"</i>
  </p>
</div>
How many of their wins for the season were not against teams with winning records?
<div>
  <p class="decomp">
   1. return the  season <br>
   2. return wins of #1 <br>
   3. return #2 that were against teams with winning records <br>  
   4. return number of  #2 <br>
   5. return number of  #3 <br>
   6. return the  difference of #4 and  #5  
  </p>
</div>


