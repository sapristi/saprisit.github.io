title: BLOG
---

## Artificial chemistries for artificial life

### Where it starts

After doing an internship at the INRIA BEAGLE Team involving artificial chemistries and artificial life, I got really caught with the subject.

I will try in the following post to describe what I remember about this field, and how I tried to circumvent the shortcomming I saw in the previous research in this field (as I write this from several years old memories, errors and imprecisions are to be expected). 


### Artificial chemistries for artificial life

An *artificial chemistry* is a program, or a mathematical model, that implements chemistry-like features. *Artificial life* on the other hand is an attempt to build such a model or program that will allow organisms to live, reproduce and evolve.

The two main objectives in artificial life are to reach :

 * open-ended evolution : the organisms should keep evolving. This implies that there must not be a « best possible organism ».
 * open-ended complexity : the organisms should keep developping new functions, new capacities.

In order to achieve this, we have to keep some ideas in mind when designing an artificial chemistry  :
 
 1. Allow the presence of evolving self-replicators.  
 2. Be as agnostic as possible regarding the organisms. This means that one should not implement functions that will implement some aspects of the life of  the organisms, because any such hard-defined function will be de facto put aside of the  evolutionary process.

One of the problems arising from the second point is about *membranes*. Membranes are a key part of any living organism : they define what is part of the organism, and what is not.  And although self-replicators have been designed in many different situations, full featured membranes are still out of reach.



### A quick overview of existing artificial chemistries

There have been several attemps to design artificial chemistries. Here is a very brief review of some of them 

 * Tierra : deeply rooted in the computer world, Tierra is an achem where the organisms are programs, living in a linear memory array.
    
  **Pros :** 
    * very fast simulation
    * organisms can interact
    * achieved some evolution in complexity

   **Cons :** 
    * evolutions stops at some point
    * Hard membranes


 * Hutton's : An artificial chemistry where atoms have different types and states, and live in a 2D world. Rules allow atoms to bind and unbind. A set of custom rules allows to implement self-reproducing organisms.
  
  **Pros :** 
    * achieved some fitness evolution
    * emerging membranes
  
  **Cons :**
    * slow simulation (although other approaches allow to speed this up)
    * lack of expressiveness

### Yet Another Achem (Yaa)

From reviewing results achieved by these chemistries (and others as well), I decided to design my own.
Here were my goals :
 * Allow for interaction between organisms
 * Allow good expressiveness
 * Allow fast simulations

A starting point to allow fast simulation is to forget the real physical world, since trajectory computations are way to eager in 2D, let alone in 3D. But the linear world on which Tierra is set is by nature very narrow. And designing multidimensional computer programs is far from trivial.

After thinking about this problem every now and then in the year following my internship, I came across...Petri nets ! 

To be continued.