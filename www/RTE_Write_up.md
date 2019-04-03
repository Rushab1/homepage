---
title: RTE and NYC Office write up - Rushab Munot
layout: post
excerpt_separator: <!--more-->
---
**Rushab Munot**  
**3rd Year Undergraduate Student**  
**Department of Computer Science and Engineering**  
**Indian Institute of Technology Kanpur**  
**Email: [rushab@iitk.ac.in](mailto:rushab@iitk.ac.in) Homepage: [Click here](http://home.iitk.ac.in/~rushab)**  

<!--more-->
<hr>

#Parameter Tying by Quantization applied to Logistiv Regression:

### Mentors:

  * Professor [Vibhav Gogate](http://www.hlt.utdallas.edu/~vgogate), Department of Computer Science, University of Texas at Dallas
  * Professor [Piyush Rai](http://www.cse.iitk.ac.in/users/piyush), Department of Computer Science and Engineering, IIT Kanpur

### Project Description

##### Introduction:
The main aspect of the project was to study parameter tying by quantization used for regularization. 

##### The Technique:

To tie parameters we need to first learn them without any regularization. Then from these parameters we decide which parameters to tie together (i.e. set some comstraint on them) and how. Then we re-learn the model.

##### The Specifics:

   * For tying parameters, the paper uses one dimensional k-means clutering. This can be done using dynamic programming in _O(n^2k)_ time. (Wang and Song, 2011)
   * Thus we get k equivalence classes
   * The constraint is that parameters in each class must have equal weights
   * The model is then re-learnt using these constraints

##### Evaluation:
   * The model was evaluated on the iris dataset, email classification, and digit recognition
   * The model works extremely well for email classification, with an maximum accuracy of about 98.3% which is more than 3% higher than that of Logistic Regression with L2 regularization which is about 95%.
   * Similar results were obtained for the iris dataset, even though it has just 4 parameters
   * However, the model fails for digit recognition
##### Papers read:
   * On Parameter Tying by Quantization (Gogate, Ruozzi, Chou, Sarkhel, 2016)
   * Dynamic Programming approach to one dimensional k means clustering (Wang and Song, 2011)
   * Feature selection, L1 vs. L2 regularization, and rotational invariance (Andrew Ng)
 
##### Project Report:

[Report](https://home.iitk.ac.in/~rushab/report.pdf), [Results for email classification](https://home.iitk.ac.in/~rushab/Results_email.pdf)

##### Project Presentation:

 [Click here](https://home.iitk.ac.in/~rushab/RTE_Presentation.pptx)

##### Software/Libraries used:

scikit-learn, Scipy, Numpy

##### Languages Used:

python

##### Version Control System:

Git

### Skills:

  * Uses of quantization for regularization
  * Theoretical aspects of quantization, some algorithms, theorems and their proofs

# Hacking/ML tasks for IIT Kanpur's New York Office:

### Mentor:

Professor [Manindra Agrawal](http://cse.iitk.ac.in/users/manindra/), Department
of Computer Science and Engineering, IIT Kanpur

### Description of Tasks:

* Automation of Phabricator Daemons

  * To debug an existing code so that phabricator daemons are launched when the code is run
  * Worked on dockers, phabricators and kubernetes - a totally new exposure*



* Feature Detection from raw html profiles

  * To detect features such as 'Name', 'Skills', 'Company', etc. from html profiles
  * Learning involved studying NLP models like tf-idf, Word2Vec, Doc2Vec
  * To find which model works better and why
  * Tried initially using only tf-idf, obtained poor results
  *  Then tried using Wor2Vec (Mikolov et al, 2013), i.e. skip gram with negative sampling and CBOW models, better results but still not up to the mark (e.g. all the names present in a given profile were printed)
  * Finally settled on skipgram with negative sampling combined with term frequencies of a word. Much better reesults.
  * As of now I am trying to improvise on the results

### Skills:

  * Dockers, basics of phabricators and kubernetes
  * NLP models - Word2Vec, Doc2Vec, their advantages and disadvantages
