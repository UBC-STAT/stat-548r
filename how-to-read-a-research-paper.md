---
layout: page
title: How to Read a Research Paper
permalink: /readings/how-to-read-a-research-paper/
---


**About:** 
Reading research papers is challenging; research papers are often **dense**, assuming significant **prior knowledge** about the field, including conventions, "standard" ideas, and related work. 
As such, it is important to
1. expect that it will be a **learning process** -- that it might take a while at first, but with practice you will improve! and
2. to adopt and practice **paper-reading strategies**.

In this guide, we outline a general strategy for paper reading. 
We hope that you will find it useful, and encourage you to ask your peers, colleagues and mentors for more insights about how they read papers, specifically in your field. As your ability to read research papers improves, reflect on the strategies you find most helpful and whether you are using any not described here. 

**Acknowledgements:** This guide is adapted from [How to Read a Research Paper](https://harvard-cs290-2025-26.github.io/readings/how-to-read-a-research-paper/){:target="_blank"}{:rel="noopener noreferrer"}, which itself adapts [Margo Seltzer's course on OS Research](https://www.seltzer.com/margo/teaching/CS508.21/intro.html){:target="_blank"}{:rel="noopener noreferrer"} and [Weiwei Pan's course on Stochastic Methods](https://docs.google.com/document/d/1MPEOSairUkktoZmX1N8zcIaENjyirt-JgRfSD-HBymk/edit){:target="_blank"}{:rel="noopener noreferrer"}.


## Paper-Reading Strategies

### Research papers are **not** meant to be read font-to-back, like a novel. 
* **First, skim.** Focus on the **high-level ideas**, jot down high-level questions you may have about the **story** told by the paper. Try not to get bogged down by details. 
* **Then, a deeper read** (if the paper seems relevant). 
* **Don't read font-to-back -- read for answers to the "guiding questions" instead.** For every paper, answer the "guiding questions" below -- answers to these questions will allow you to construct a **story / narrative** the paper is telling.
* **Read actively.** Reading a paper is not a passive process. Compare what the paper says with what you already know, and when you find a contradiction, try to understand where it comes from (e.g., an assumption?). Draw pictures / diagrams of what the paper describes as you're reading to check your understanding against the paper -- often you'll find that in doing so, you will be able to translate a general feeling of confusion into concrete questions that, if resolved, will give you a clear understanding of the paper. 
* **When confused...** You may be missing information assumed to be "commonly known" by the intended research community / audience. If you can identify a specific gap in understanding, you will be able to address it directly. We recommend that you try to **fill in the gap** by looking for related papers (e.g., ones cited by the paper you're reading, ones that share key-terms on google), wikipedia pages, blog posts, lectures on youtube, etc. For papers that are very long, you may additionally find shorter conference versions that convey the general story more concisely and may contain all you need. For technical material used in the paper, finding a good textbook can help. (Does the paper cite one?) There's no formula here, but going back and forth between reading related material and the original paper of interest can help you get unstuck.

### Stay organized -- keep track of what you've already read:
* Save your future-self time and take notes that will help you dig deeper every time you re-visit the paper. 
* Different people find different organizational methods useful, but some common ones are:
  - Taking notes on the paper, underlining, without focus on being neat -- this can help you understand the paper better as you go!
  - Keeping a **searchable doc** (e.g., Evernote) in which you summarize the paper / answer the paper-reading questions below -- this will help you pick up a paper where you left off.
  - Using a **citation manager** (e.g., Zotero) to keep lists of paper and easily create latex bibliographies -- this will save you time when writing your own paper.
* For every paper, especially focus on recording:
  - The "big ideas"
  - Relevant buzz words
  - Story / narrative (answers to the "guiding questions")
  - Where it fits into the larger body of research

### Ask lots and lots of questions:
* You're here to **learn** how to read papers and are *not expected to already know how to do it*.
* Reading research papers is challenging: they are often very dense and assume significant prior knowledge about the field and about related work. It is important to ask questions about the paper you read, and actively look for tips about others' paper-reading strategies! 
* It is expected and normal that when you first start reading research papers in a new field, it will take you several hours to get through a paper. If it takes you a long time to read a paper, you're not alone!
* Discussing papers informally at reading groups or journal clubs, and with fellow researchers can help you understand them more deeply. (And realize that you aren't alone in finding it challenging!)


## Guiding Questions

We recommend of thinking of "paper reading" as *the process of answering the following guiding questions*.
Whether you are skimming or deep-reading, these guiding questions will help you re-construct the narrative told by the paper.
By practicing answering these questions for every paper you read, you will practice quickly honing in on the meaning behind the paper instead of being bogged down by details. 

### What kind of paper are you reading? 
By understanding the type of the paper, you can anticipate its structure and evaluation, which will help you determine which parts to 
on during your initial skim. (Many papers will have aspects of multiple of these.)
* Big idea 
* "Small" idea with evaluation (most papers)
  * Improved implementation of an existing method
  * Fixes a shortcoming of an existing method
* Empirical evaluation of existing methods
* New dataset or benchmark test
* New software package (there are often dedicated venues for these)
* Retrospective or experience paper
* Proposes a new model or type of problem for study 
* Solves (or partially solves) a known open problem
* Points out a failure or shortcoming of existing methods
* Clarifies or simplifies our understanding of a known result or phenomenon
* New techniques for proofs
* Unifying theme
* Review article
* Other?
* Is the paper in a statistics journal (theory, methods, applications?), a machine learning conference, or another venue?
  - The venue will affect how the paper is written (target audience, conventions, etc.), how results are presented, what the relevant literature is, etc.

### Motivation and Potential Impact 
* What is the problem the paper addresses?
* Why is this problem important?
* If a theory or methods paper, what are the formal definitions and assumptions, and how well do they capture the phenomenon of interest?

### Related Work and Contributions 
* How is the problem traditionally solved?
* Why are existing approaches not good enough?
* At a high level, how does the paper address the problem?
* Can the ideas or techniques from this paper be used to address other problems?

### Results (Theory and/or Experiments)
* Theory
  - What types of theory is developed? (E.g., properties of a new model, statistical theory for a method, etc.)
  - What are the main theorems in the paper?
  - Is there a new proof technique?
  - At a high level, how do the theorems relate to earlier results?
* Methods
  - What are the main methods in the paper? 
  - Is there a new model on which the method is based?
  - At a high level, how do the methods relate to earlier approaches?
* Experiments
  - How does the paper define success?
  - How is success measured?
  - What approaches does the paper compare against (and why)?
  - What is the experimental design?
  - At a high level, what are the results?

### Broader Impact
* Identify the relevant socio-technical systems
  - Where could the technology be deployed, or which kind of technology is informed by the paper (if a theoretical paper)?
  - How would this technology be used?
* Identify the stakeholders
  - Who would be the users?
  - Who would be the affected communities (are these the users)?
* What types of good can this technology do?
  - What kinds of needs do these users/businesses/communities have?
  - What kinds of constraints do these users/businesses/communities have?
* What types of harm can this technology do?
  - What kinds of failures can this technology have?
  - What kinds of direct harm can these failures cause?
  - What kinds of harm can be caused by the broader, socio-technical system?

### What questions do you have? E.g.,
* What "holes" are there in your understanding of the paper's narrative? (e.g., the paper claims that traditional methods cannot solve the problem, but you don't see why they don't suffice? The paper claims the problem is important, but you don't see why?, etc.)
* What are unfamiliar terms used in the paper that seem important?

### Lastly, what did you learn from the paper?




## Deeper reading and Critiquing a Paper

After answering the above guiding questions, additionally answer the following questions:

* **The ideas:**
  - Do the ideas make sense?
  - Are the ideas well-motivated?
* **The methodology:**
  - Are the high-level ideas behind the proposed approach / method sound (i.e., do they seem plausible)?
  - If a **theoretical** paper, does the theory presented support the claims of the paper:
    - Are the theorems proved the "right ones" to support the claims? (Many times, this boils down to the assumptions.) 
    - If not, do the authors discuss why they proved this theorem and not another one?
    - Do the proofs appear to be technically sound, complete, and are they reasonably clear to read?
    - How are the main theorems constructed? (It can help to draw a dependency graph of all results in the paper.)
    - How do the proof techniques work?
    - Where (in the proofs) are the assumptions used? How much "work" are they doing? Could they be weakened? 
    - Is there a new proof technique? Is the proof technique familiar to you (perhaps from related work or a different area)?
    - Is the theory adequately situated in the context of the existing literature?
  - If a **methods** paper, does the method presented support the claims of the paper:
    - Is the method applicable in the "right settings"?
    - Is it computationally feasible?
    - Are the data requirements reasonable?
    - Does it require any (additional) probabilistic/statistical/mathematical modeling assumptions?
    - Does the method resemble (or is it inspired by) existing methods?
  - If an **experimental** paper, do the results support the claims of the paper:
    - Are the problem instances studied suitably representative of and/or applicable to the phenomenon of interest? 
    - Do the results generalize? Or do they only hold in the cases studied in the paper?
    - Do the baselines represent state-of-the art approaches to this problem?
    - Are the evaluation metrics measuring the right things? 
    - Do the experiments provide evidence that it is the innovations introduced in this paper that cause the improved performance?
    - Are there statistical issues with:
      - the experimental design?
      - the analysis of experimental data?
      - conclusions drawn from the experimental results?
* **The contribution:**
  - Are the authors' claimed contributions supported by the paper's results?
  - Does the paper solve/address the problem it sets out to address?
* **Presentation:**
  - Are the ideas presented clearly?
  - Is mathematical notation used properly and clearly? 
  - Is the relevant related work cited properly?