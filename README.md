# Conversational Sarcasm Corpus (CSC)

--- 
### 1. List of files: 

There are 3 files in **.tsv**, **.csv** or **.json** format. \
**.tsv** files include demographic information. \
**.csv** and **.json** files do not have demographic information (same content in either).


   * tsv
   1. data_part1_w_demo.tsv
   2. data_part2_w_demo.tsv
   3. data_full_w_demo.tsv

  * csv
    
    1. data_part1.csv 
    2. data_part2.csv
    3. data_full.csv

  * json
    
    1. data_part1.json
    2. data_part2.json
    3. data_full.json

---

### 2. Data descriptions


   * Conversational Sarcasm Corpus (CSC) was collected in two distinct psycholinguistic studies. Each study conducted experiments testing different hypotheses.
   
   * <data_full> is a compilation of both studies. It only contains *context* + *response* + *self-rated sarcasm score* + *other-rated sarcasm score*.
   
   * <data_part1> and <data_part2> have additional information collected from their respective experiments.

   * <data*_w_demo> contain demographic information about speakers (sarcasm producers) and external evaluators. There are missing data values in these files.

---

### 3. Column descriptions

   * **Columns in all files**

       * *global_context_name*: Context ID (101-132; 201-268)
       * *context_type*: Non-neutral (sarcasm-triggering) / neutral
       * *context_text*: Text of context
       * *global_speaker*: Responder ID
       * *response_text*: Text of response
       * *global_evaluator*: Evaluator ID
       * *interlocutor_relationship*: Best friend / colleague
       * *sarcasm_score_by_speaker*: Sarcasm score by speaker (=responder)
       * *sarcasm_score_by_evaluator*: Sarcasm score by evaluator
       * speaker_sex: speaker's gender
       * speaker_age: speaker's age
       * speaker_ethnicity: speaker's ethnicity
       * evaluator_sex: evaluator's gender
       * evaluator_age: evaluator's age
       * evaluator_ethnicity: evaluator's ethnicity
      
---
* **Notes**

  ** In <data_part1> there are 6 evaluators for each context+response pair. \
  ** (In <data_part1_w_demo>, there are context+response pairs having less than 6.) \
  ** In <data_part2> there are 4 evaluators for each context+response pair. \
  ** Gender in Part1 is either female, male, non-binary, or prefer not to say. Gender in part2 is female or male. \
  ** In <data_part1> and <data_part2> there are local IDs of speakers and evaluators (different from global IDs). If you are using both parts, you should use global IDs to avoid overlapping of the local IDs.

---
  * **Columns specific to <data_part1>**

    * *silly_or_annoying (_by_speaker /_by_evaluator)*: How silly or annoying the speaker (=responder) or the evaluator found the situation.
    * *intentions (_by_speaker /_by_evaluator)*: The intentions behind the remark of the speaker (=responder), judged by the speaker or the evaluator.
    * *b5**: Big Five Personality Test (John, O. P., Donahue, E. M., & Kentle, R. L.,1991) scores averaged from 2 questions for each of the 5 dimensions - agreeableness, conscientiousness, extraversion, neuroticism, openness.

---
  * **Columns specific to <data_part2>**

    * *funny (_by_speaker /_by_evaluator)*: How funny the speaker (=responder) or the evaluator found the situation.
    * *annoying (_by_speaker /_by_evaluator)*: How annoying the speaker (=responder) or the evaluator found the situation.
    * *clever (_by_speaker /_by_evaluator)*: How much intention to sound clever the speaker (=responder) had, judged by the speaker or the evaluator.
    * *mock (_by_speaker /_by_evaluator)*: How much intention to mock the speaker (=responder) had, judged by the speaker or the evaluator.
            
      ** *clever* and *mock* only exist for 20% of the whole set. 


            
---      
### 4. Scale descriptions 

  * All scales were collected from 1 - 6 Likert scale.
    
      1 (not at all) \
      2 (mostly not) \
      3 (not so much)  \
      4 (somewhat) \
      5 (mostly) \
      6 (completely) 

 * For Big Five Personality questions, the text coding for 1 - 6 was *strongly disagree - disagree - somewhat disagree - somewhat agree - agree - strongly agree*.

  * Intentions were collected as multiple-choice questions. There are 8 intentions in total:

    1. to criticize harsher 
    2. to criticize softer 
    3. to mock in a hilarious way 
    4. to mock in a friendly way 
    5. to say something clever 
    6. to be natural 
    7. to be direct 
    8. to be nice
   

---
### 5. Citations - If you use this dataset, please cite the following papers: 

<br/>

1. https://aclanthology.org/2024.naacl-long.238/


   @inproceedings{jang-frassinelli-2024-generalizable,\
    title = "Generalizable Sarcasm Detection is Just Around the Corner, of Course!",\
    author = "Jang, Hyewon  and
      Frassinelli, Diego",\
    editor = "Duh, Kevin  and
      Gomez, Helena  and
      Bethard, Steven",\
    booktitle = "Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers)",\
    month = jun,\
    year = "2024",\
    address = "Mexico City, Mexico",\
    publisher = "Association for Computational Linguistics",\
    url = "https://aclanthology.org/2024.naacl-long.238",
    pages = "4238--4249",\
}

<br/>

2. https://escholarship.org/uc/item/1cw1m8bm
   <br/>

   @inproceedings{jang2023intended,\
  title={Intended and Perceived Sarcasm Between Close Friends: What Triggers Sarcasm and What Gets Conveyed?},\
  author={Jang, Hyewon and Braun, Bettina and Frassinelli, Diego},\
  booktitle={Proceedings of the Annual Meeting of the Cognitive Science Society},\
  volume={45},\
  number={45},\
  year={2023}\
}

! *<Errata for paper #2>*

In Table 3, the significance for two variables in Experiment 2 require the following corrections: 'criticize harsher' (*) and 'context:crit.harsher' (**). The directions of the coefficients remains the same. Therefore, the corrected results indicate that **the intention to criticize, either harsher or softer, is a predictor of higher sarcasm ratings for observers**. 



