## Explore Break

Below you will find examples of questions and their QDMRs found in Break.   
Note that *high-level* QDMRs are less coarse in their decomposition, as they are geared towards reading comprehension tasks. For more details on *high-level* QDMRs please refer to [our paper](https://allenai.github.io/Break/#paper).

* **Semantic Parsing**: 
  * [Academic](#academic)
  * [ATIS](#atis)
  * [GeoQuery](#geoquery)
  * [Spider](#spider)
* **Visual Question Answering**: 
  * [CLEVR-humans](#spider)
  * [NLVR2](#spider)
* **Reading Comprehension (and KB-QA)**: 
  * [ComQA](#comqa)
  * [ComplexWebQuestions](#complexwebquestions)
  * [DROP](#drop)
  * [HotpotQA](#hotpotqa)  


### **Academic**

<div>
  <p class="note">
    <i>Return me the total citations of papers in the VLDB conference before 2005.</i>
  </p>
</div>

```
 1. return papers  
 2. return #1 in the VLDB conference   
 3. return #2 before 2005   
 4. return citations of #3  
 5. return number of #4 for each #3   
 6. return sum #4
```

### **ATIS**


<div>
  <p class="note">
    <i>What flight do you have from atlanta to dallas on august twenty seventh in the morning</i>
  </p>
</div>

```
 1. return flights
 2. return #1 from atlanta  
 3. return #2 to dallas  
 4. return #3 on august twenty seventh  
 5. return #4 in the morning
```

### **GeoQuery**


<div>
  <p class="note">
    (a) <i>Which state has the least population density</i>
  </p>
</div>

```
 1. return states  
 2. return population densities of #1  
 3. return #1 where #2 is the lowest
```


<div>
  <p class="note">
    (b) <i>What states border states that border states that border florida</i>
  </p>
</div>

```
 1. return florida  
 2. return border states of #1   
 3. return border states of #2   
 4. return border states of #3 
```

### Spider 

<div>
  <p class="note">
    (a) <i>List the name, born state and age of the heads of departments ordered by age.</i>
  </p>
</div>

```
 1. return departments  
 2. return heads of #1   
 3. return names of #2   
 4. return born states of #2   
 5. return ages of #2   
 6. return #3 , #4 , #5   
 7. return #6 sorted by #5
```

<div>
  <p class="note">
    (b) <i>Show the positions of the players from the team with name "Ryley Goldner".</i>
  </p>
</div>

```
 1. return teams   
 2. return names of #1   
 3. return #1 where #2 is Ryley Goldner   
 4. return players of #3  
 5. return positions of #4
```

<div>
  <p class="note">
    (c) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

### CLEVR-humans


<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```


<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

### NLVR2

<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

<div>
  <p class="note">
    (b) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

<div>
  <p class="note">
    (c) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

### ComQA


<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```


<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

### ComplexWebQuestions


<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```


<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

### DROP

<div>
  <p class="note">
    (a) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

<div>
  <p class="note">
    (b) <i>How many of their wins for the season were not against teams with winning records?</i>
  </p>
</div>

```
 1. return the season  
 2. return wins of #1  
 3. return #2 that were against teams with winning records    
 4. return number of #2  
 5. return number of #3  
 6. return the difference of #4 and #5  
```

### **HotpotQA** (*high-level*)

<div>
  <p class="note">
    (a) <i>How old was William DuVall when Black Gives Way to Blue was certified gold by the RIAA?</i>
  </p>
</div>

```
 1. return when Black Gives Way to Blue was certified gold by the RIAA  
 2. return how old was William DuVall on #1 
```

<div>
  <p class="note">
    (b) <i>Did the Battle of Peleliu or the Seven Days Battles last longer?</i>
  </p>
</div>

```
 1. return how long did the Battle of Peleliu last  
 2. return how long did the Seven Days Battle last  
 3. return which is longer of #1 , #2
```

<div>
  <p class="note">
    (c) <i>The Love Machines stars an actor born in 1926, known for his nightclub performances in what city?</i>
  </p>
</div>

```
 1. return the actor born in  1926 that stars in the Love Machines  
 2. return the nightclub performances that #1 was known for  
 3. return in  what  city was  #2
```
