## Explore Break

Below you will find examples of questions and their QDMRs found in Break.   
Note that *high-level* QDMRs are less coarse in their decomposition, as they are geared towards reading comprehension tasks. For more details on *high-level* QDMRs please refer to [our paper](https://allenai.github.io/Break/#paper).

* **Semantic Parsing**: 
  * [Academic](#academic)
  * [ATIS](#atis)
  * [GeoQuery](#geoquery)
  * [Spider](#spider)
* **Visual Question Answering**: 
  * [CLEVR-humans](#clevr-humans)
  * [NLVR2](#nlvr2)
* **Reading Comprehension (and KB-QA)**: 
  * [ComQA](#comqa)
  * [ComplexWebQuestions](#complexwebquestions)
  * [DROP](#drop)
  * [HotpotQA](#hotpotqa)  


### **Academic**

<div>
  <p class="note">
    Return me the total citations of papers in the VLDB conference before 2005.
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
    What flight do you have from atlanta to dallas on august twenty seventh in the morning
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
    (a) Which state has the least population density
  </p>
</div>

```
 1. return states  
 2. return population densities of #1  
 3. return #1 where #2 is the lowest
```


<div>
  <p class="note">
    (b) What states border states that border states that border florida
  </p>
</div>

```
 1. return florida  
 2. return border states of #1   
 3. return border states of #2   
 4. return border states of #3 
```

### **Spider** 

<div>
  <p class="note">
    (a) List the name, born state and age of the heads of departments ordered by age.
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
    (b) Show the positions of the players from the team with name "Ryley Goldner".
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
    (c) Find the total number of students enrolled in the colleges that were founded after the year of 1850 for each affiliation type.
  </p>
</div>

```
 1. return affiliation types  
 2. return colleges of #1   
 3. return #2 founded after 1850   
 4. return students enrolled in #3   
 5. return number of #4 for each #1
```

### **CLEVR-humans**


<div>
  <p class="note">
    (a) How many silver spheres are not the smallestt shape?
  </p>
</div>

```
 1. return spheres   
 2. return #1 that are silver   
 3. return size of #2   
 4. return #2 where #3 is the lowest  
 5. return #2 besides #4   
 6. return number of  #5
```


<div>
  <p class="note">
    (b) What one color are four of the objects?
  </p>
</div>

```
 1. return objects  
 2. return colors of #1   
 3. return number of #1 for each #2   
 4. return #2 where #3 is four
```

### **NLVR2**

<div>
  <p class="note">
    (a) If there are no more than 5 and no less than 2 televisions in a single image.
  </p>
</div>

```
 1. return images  
 2. return televisions in #1   
 3. return number of #2 for each #1   
 4. return #1 where #3 is at most 5   
 5. return #1 where #3 is at least 2   
 6. return #1 in both #4 and #5   
 7. return number of #6  
 8. return if #7 is equal to  one
```

<div>
  <p class="note">
    (b) If one person is riding a bicycle near two dogs.
  </p>
</div>

```
 1. return people  
 2. return bicycle  
 3. return #1 riding #2   
 4. return dogs   
 5. return #3 near #4   
 6. return number of #4 for each #5   
 7. return number of #5  
 8. return if #6 is equal to two    
 9. return if #7 is equal to one   
 10. return if both #8 and #9 are true
```

<div>
  <p class="note">
    (c) If there are an equal number of dogs in each image.
  </p>
</div>

```
 1. return images  
 2. return dogs in  #1  
 3. return number of #2 for each #1  
 4. return if #3 are equal
```

### **ComQA**


<div>
  <p class="note">
    (a) Who was the first president to serve 3 terms?
  </p>
</div>

```
 1. return presidents  
 2. return terms of #1  
 3. return number of #2 for each #1    
 4. return #1 where #3 is equal to 3   
 5. return first of #4
```


<div>
  <p class="note">
    (b) Birthdates of george pattons kids?
  </p>
</div>

```
 1. return george patton   
 2. return kids of #1   
 3. return birthdates of #2
```

### **ComplexWebQuestions**


<div>
  <p class="note">
    (a) What country is the composer of Up Out My Face from?
  </p>
</div>

```
 1. return Up Out My Face   
 2. return composer of #1   
 3. return country of #2
```


<div>
  <p class="note">
    (b) What do most people speak where the Nigerian pound is used?
  </p>
</div>

```
 1. return the Nigerian pound   
 2. return where is #1 used 
 3. return what do most people speak in #2
```

### **DROP**

<div>
  <p class="note">
    (a) What event happened first, Jabal Shammar being annexed or the preliminary attack on Taif?
  </p>
</div>

```
 1. return Jabal Shammar being annexed  
 2. return the preliminary attack on Taif  
 3. return when was #1  
 4. return when was #2   
 5. return which is lowest of #3 , #4
```

<div>
  <p class="note">
    (b) How many years passed between rebellion breaking out at Pegu and Pegu began their annual raids?
  </p>
</div>

```
 1. return the rebellion breaking out at Pegu   
 2. return Pegu began their annual raids   
 3. return year of #1   
 4. return year of #2 
 5. return difference of #4 and  #3
```

<div>
  <p class="note">
    (c) Who threw the most touchdowns in the first half?
  </p>
</div>

```
 1. return touchdowns   
 2. return #1 in the first half   
 3. return who threw #2   
 4. return number of #2 for each #3   
 5. return #3 where #4 is highest
```

### **HotpotQA** (*high-level*)

<div>
  <p class="note">
    (a) How old was William DuVall when Black Gives Way to Blue was certified gold by the RIAA?
  </p>
</div>

```
 1. return when Black Gives Way to Blue was certified gold by the RIAA  
 2. return how old was William DuVall on #1 
```

<div>
  <p class="note">
    (b) Did the Battle of Peleliu or the Seven Days Battles last longer?
  </p>
</div>

```
 1. return how long did the Battle of Peleliu last  
 2. return how long did the Seven Days Battle last  
 3. return which is longer of #1 , #2
```

<div>
  <p class="note">
    (c) The Love Machines stars an actor born in 1926, known for his nightclub performances in what city?
  </p>
</div>

```
 1. return the actor born in 1926 that stars in the Love Machines  
 2. return the nightclub performances that #1 was known for  
 3. return in what city was #2
```
