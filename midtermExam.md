# Midterm Examination for Computer Science 102 Fall 2022

## Name
Add Your Name Here

## Dates

Handed out: 28 October 2022

Due: 29 October 2022, 11:59pm

Please note the following.

* In this midterm, you are not allowed to discuss your work with others.

* There are several questions following each coded exercises. Please replace the "to-do's" with your responses.

* The exam is due at the deadline. Missing exams will receive a zero.

* Each question on the test is worth 5.0 pts.
  + Q's x 20

* Best of luck.

## Questions for the Midterm Examination

---

# 1 The Strings-db protein analysis tool 

We will create a STRING network for human insulin receptor (called, __INSR__) using the tool at [https://string-db.org/](https://string-db.org/).

Click "SEARCH" on the welcome page to begin. Locate and click on the _Protein by name_ tab. In the _Protein Name_ search field, enter "INSR" and in  the _Organisms_ field, you can specify "Homo sapiens" or leave it at "auto-detect". Click "SEARCH".

You will find a disambiguation page where the organism of interest is to be selected. Specify "Homo Sapiens" human protein INSR, if this is not already specified. Note this option is likely to be found at the top of the list. Click "Continue" to create the protein network.

---
### Q1

Describe the network that appears. For instance, what are the nodes, what are the edges?

```
TODO
```
---

## Visual representations

The STRING web interface provides differing visual representations of protein networks. Use the "Setting" tab to alter the type of visual representations of the network by changing the types of nodes, edges, and the interaction types.

Try changing the options in the rubric called, "Meaning of network edges". For instance switch from "evidence" to "confidence" to determine differences. Click  "UPDATE" button after a change.

---
### Q2
What is the difference between the "evidence" and the "confidence" settings?
```
TODO
```

### Q3

How could each of these networks be useful (in absence of the other) in a protein research project? Can you think of a concrete example where protein knowledge can be gained from each of the network types?
```
TODO
```


### Q4

What is the purpose of the confidence level in the "Minimum required interaction score" drop-down menu?

```
TODO
```


### Q5

Try changing the confidence setting from 0.9 to 0.7 and update the network. Describe and explain the outcome of this change.

```
TODO
```
---

## Evidence viewers

A helpful feature of the STRING web tool is provided by the evidence viewers of the "Viewers" tab.

---
### Q6

Which types of evidence support the interaction between insulin receptor (INSR) and insulin receptor substrate 1 (IRS1)?

```
TODO
```


### Q7

In your opinion, which form of evidence of connectivity would be more appropriate to a pilot study which has been designed to explore the protein network. For example, are there different levels of evidence in research? Explain your reasoning.

```
TODO
```
---


Further detail on the evidence of an interaction can be seen in a popup by clicking on the corresponding edge in the network (when the "Meaning of the network edges" is set to "confidence").

Try clicking on the edge between INSR and IRS1 to view its popup. Note, it might be necessary to move the nodes around to be able to get to the edges.


### Q8

What is the connection between these two nodes?

```
TODO
```

Click on the "Show" button to view the experimental evidence for the interaction.

### Q9

Which types of experiments do you find here to make a case for the existence of an interaction? 

```
TODO
```
---

## 4 Query settings

In addition to the network view, the set of "interactors" can also be viewed in a tabular form. Go back to the network graphic and click on the "Legend" tab to find several tables below the network graphic.

---
### Q10

How many _Predicted_ functional partners are shown for INSR? 

```
TODO
```

### Q11
What types of information is used to suggest that the Functional Partners are _Predicted_? Hint: you might have to return to an earlier page to determine information about how relationships are "Predicted."

```
TODO
```
---


Change back to the "Settings" tab. Change the "minimum required interaction score" to 0.7 if it is not already set at this value.

Change the "max number of interactors to show" to 50. Click "UPDATE" to apply the changes. Then go to the "Analysis" tab.

---
### Q12

Your network will have changed. What kinds of information is now available under the "Analysis" tab?

```
TODO
```
---

While keeping the same network from above of over 50 nodes on your screen, click on the "Clusters" tab. Select the "k-means clustering" option and set the number of clusters to 4, 6 and finally to 10. Click "Apply" after each setting to observe the changes that each value brings.

---
### Q13

In clear and meaningful language, please explain what is happening when the "k-means" option is being run for different integer values? In other words, what is the difference between small and large k-means values?

```
TODO
```

### Q14

How can using k-means be helpful to a research project? Please give an example of a potential benefit.

```
TODO
```
---

# 2. Unknown sequences

You are a world-famous researcher who specializes in determining the names and (likely) origins of unknown sequences of DNA. Two unknown sequences have just arrived for your attention (see `seq_1` and `Seq_2` in text below, and also in the `data/` directory of this repository.

Your task is to use tools of your choice to determine what these sequence are, and where they have come from.

Hint: In class, we have been using tools made available from [https://www.ncbi.nlm.nih.gov/](https://www.ncbi.nlm.nih.gov/).


__First Sequence__

```
>Seq_1
ATGCTGTGGTGGCTAGTGCTCCTACTCCTACCTACATTAAAATCTGTTTTTTGTTCTCTTGTAACTAGCC
TTTACCTTCCTAACACAGAGGATCTGTCACTGTGGCTCTGGCCCAAACCTGACCTTCACTCTGGAACGAG
AACAGAGGTTTCTACCCACACCGTCCCCTCGAAGCCGGGGACAGCCTCACCTTGCTGGCCTCTCGCTGGA
GCAGTGCCCTCACCAACTGTCTCACGTCTGGAGGCACTGACTCGGGCAGTGCAGGTAGCTGAGCCTCTTG
GTAGCTGCGGCTTTCAAGGTGGGCCTTGCCCTGGCCGTAGAAGGGATTGA
```

__Second Sequence__

```
>Seq_2
GGGGGGTTTAACCAGCGTAGACATATTGCCAACGAATTTACAGTCCGTCCCCATTGACCGCTCGGGCATC
GACCCAGGAAGAATCCACTTTAGGCTTATTGGGAATCCATGATCAACTTCCTTTCGTAGTACCCTACCCC
CAGGGGAATTCGAATCCCCGCTTCCTCCTTGAAAGAGAGATGTCCTAAACCACTAGACGATGGGGGCCGA
CTTGTCCAACTGCCGTGATACTATCATCATAGTATGATCAGGTTTTTAAAATTGTCAATAGAATAGAATG
ATATGAATAAATCCGAGGGATATTAAAAATTGTATCGAATTTTTAGTTCATTATTTAATTCCTCAATCGT
TCGTTTAGTAATATTAGAATCTTTATATAAATCTAGTAAGCGGTAGAACGAAATTAGCGACAGTTGTCTC
TAAGACTTTAGTTTAGTTCAAGAGTACAGGACACATATAATCTCTTCCAATTCAATGAAATATCGGGAAA
TTTTTTTTAGATCGAATTCGTAAGTCTACATGTATGTTATTATTAATTAAGTGAATTTTGTTTTGATAGA
AAGCATCTCAATAAAAGAAGCCGGTATTCAAACAATTGATTTTATATTAGATTTGCTCTACACCATTTGA
TTATTCAATAATCAGCGACTAGCCAGTATGAGTCTACTATCTATACTTATGGATTGTATATAATGTCTAT
TATTATTATATCCATAGACATAGCAACTCATTCGGTAATGAAATAAAACAAGCCCTTT
```


---
## Q15
Identify `Seq_1` by is description or name.

```
TODO
```

## Q16
From which organism was this sequence most likely extracted?

```
TODO
```

## Q17
Offer a justification that your description and origin information is correct about this sequence.

```
TODO
```

## Q18
Identify `Seq_2` by is description or name.

```
TODO
```

## Q19
From which organism was this sequence most likely extracted?

```
TODO
```

## Q20
Offer a justification that your description and origin information is correct about this sequence.

```
TODO
```
---

(Did you remember to put your name at the top of this document?)