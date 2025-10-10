---
layout: page
title: Design and Presentation of Computational Experiments in Statistics/ML
permalink: /readings/computational-experiments/
---


**About:** 
Evaluating a new stats/ML method often requires a set of computational experiments. The purpose(s) of experiments is not always clear to new (and experienced!) researchers. This guide provides an overview of what can be accomplished with experiments, and provides high-level strategies for designing experiments and presenting results. (Note: I am not using "design of experiments" in the technical sense here, though such considerations should be present.)


## Computational experiments: what, why, when, where, how?

You are writing a paper on your new method for Doubly Robust Causal Representation Augmented Generative diffusion modelling, or DR CRAG for short. You've done a bunch of computational experiments as part of the research project, and after some initially middling results, things are looking great. 

- **What does "looking great" mean?** It can take many specific forms, but at a high level, your experiments should provide reproducible evidence that your method (partially) solves the problem you set out to solve. See the next section for an overview of some common types of experiments. 
- **Why do we need experiments?** Unless you're writing a paper that is purely theoretical *and* experiments would not add any value to the paper (in which case you should say so from the beginning, but still be prepared for a reviewer who will insist that "there aren't enough experiments"), experiments are required to help bridge the gap from "Here's an idea I had" to "Here's a new method that performs well on Problem A and still leaves open the question of how to do better on Problem B." Empirical evidence is indispensable in scientific inquiry, and computational experiments are the stats/ML methods equivalent of laboratory experiments in the natural sciences. 
- **When should I run experiments?** Throughout the project! Experiments should go hand-in-hand with conceptual and theoretical development. They can help build intuition, validate theory, help you refine the problem scope, etc.
- **When should I run the experiments that will go in the paper?** Although a subset of your research-in-progress experiments (previous bullet point) may make it into the paper in some form, the paper-worthy experiments should almost always be performed while you're writing the paper. Why? Because the experiments you report should be part of a coherent narrative that starts in the introduction, and the main claims of the narrative will need to be supported by a mix of theory and experiments. *This is a major difference between stats/ML methods research and experimental sciences research*, the latter of which typically writes a paper around reporting the results of experiments that were already performed. 
- **Where should I report experimental results?** Typically, the results of experiments are presented near the end of a paper, after everything else has been said. They play the role of supporting arguments made earlier, deepening understanding, and demonstrating limitations. A well-placed smaller experiment in earlier sections can help motivate a problem, demonstrate limitations of existing methods, etc. It is also somewhat common in ML papers now to have a "win" plot on the first page, though I don't use this approach. 
- **How should I report experimental results?** In the same way as you've written the rest of the paper: clearly, minimizing unnecessary cognitive load, and in a way that readers in your field will find relatively easy to understand. Every (sub-)field has its conventions, so look at how results are presented in related papers---but don't feel obligated to propagate bad conventions! Some rules of thumb: 

	+ pictures are better than numbers; and
	+ numbers are more precise than pictures.

Include enough detail on the experimental set-up so that a reader can understand the most important ideas, but not so many that they get distracted by minutiae. (Include those minutiae in the appendix/supplement and, better yet, put your code on Github and include files that have the experimental settings need to reproduce the results in the paper.)


In short, your experiments should support your claims and help provide understanding of properties/advantages/disadvantages. They should also be reproducible. (This does not mean that the exact numbers should necessarily be reproducible, but that a competent researcher can use your code and/or write code based on your paper and obtain qualitatively similar results.)


## Types(s) of computational experiments

One of the great things about computational experiments is that interventions are usually easy to make. Modifications to data, model, method, etc., require programming (often a small amount) rather than setting up a new laboratory experiment. 

Here are some common types of experiments. 


### Proof-of-concept

**Purpose**: Demonstrate that your new method (DR CRAG) works in a relatively simple setting. 

What's a simple setting? Maybe:

- the "ground truth" is known (e.g., can be worked out analytically, computed with a very expensive method, or is known because you generated the data); or
- the problem is already essentially "solved" by existing methods in this setting.

**Examples**: 

- Your computationally efficient method agrees with a gold standard method that requires much more computation.
- Your estimator/hypothesis test/new model/etc. does what you claim it does (is unbiased, consistent, powerful, data-efficient, etc.) on synthetic data that you have generated to have specific properties. 

### Highlighting a specific feature and supporting claims

**Purpose**: Demonstrate that DR CRAG has the properties you claim it does.


**Examples**: 

- Theorem 3, that says that DR CRAG is symmetry-preserving? Here's your chance to demonstrate that.
- DR CRAG makes weaker assumptions than existing methods? Demonstrate the practical consequences of that. 


### Benchmarking (and leader-boards)

**Purpose**: Measure the performance of DR CRAG on a benchmark task (or tasks) that the field agrees (perhaps implicitly) is important. 

This is common in ML research. There is a tendency (especially among less experienced researchers) to consider your DR CRAG paper unpublishable if DR CRAG is not state-of-the-art (SOTA), i.e., at the top of a benchmark task leader-board. This view is fraught with problems and there has been pushback in recent years, but it is still present. Keep in mind that a new method *does not* need to be unequivocally SOTA; there is scientific value in a method that deepens our understanding, performs well only in some settings (which?), achieves a good trade-off in performance under resource constraints, operates with weaker assumptions, etc. Benchmarks are useful for making comparisons between methods, but the story does not end with the leader-board. 

<!-- **Examples**:

- Bivariate causal discovery: various synthetic data generating procedures and real data [Tuebingen cause-effect pairs](https://webdav.tuebingen.mpg.de/cause-effect/)
- Computer vision: 
- Reinforcement learning: 
-  -->

### Demonstration on real data

**Purpose**: Various.

From the submission information pages of two leading stats methods journals (emphasis mine):

- [From JRSS B](https://academic.oup.com/jrsssb/pages/general-instructions): "Many papers published in Series B present new methods of collecting or analysing data, with associated theory, an indication of the scope of application, and a *real example*."
- [From JASA Theory and Methods](https://www.tandfonline.com/action/authorSubmission?show=instructions&journalCode=uasa20): "Illustration of techniques with *real data* is especially welcomed and strongly encouraged."

It is a time-honored tradition in stats/ML to evaluate a new method on *real data*. The fact that we need to specify that the data are real (as opposed to synthetic) should indicate that the exercise is both sensible but somewhat silly: we're statisticians so we can't just be doing math and simulating things, but we're also not domain experts so no real science is being done in the analysis. This is almost entirely proof-of-concept but without the experimental control or domain expertise to come to any real conclusions. If your method really can be used to advance the knowledge of a scientific field, either you're already collaborating with folks from that field, or you should go seek them out!

In ML research, either you're in a situation similar to the one above, or you're working for a company that won't let you actually use the real data in your paper. 


### Ablation studies

**Purpose**: Attribute performance/properties to different components of the method. 

[Ablation](https://en.wikipedia.org/wiki/Ablation_(artificial_intelligence)){:target="_blank"}{:rel="noopener noreferrer"} is a term that gets used a lot in AI/ML research, though many other fields use similar ideas. Functionally, it means removing a part of a system and assessing performance of the resultant system. Used in the context of experimenting with a new stats/ML method, the difference in performance between the full system and the "degraded" system is causally attributed to the ablated (i.e., removed) part. 

DR CRAG relies on doubly robust estimation *and* Causal Representation Augmented Generative diffusion modelling (whatever that might mean). Does the performance of DR CRAG rely on both? Only one? Neither? 


### Limitations of method

No method is perfect. Reviewers are (rightfully) skeptical of a paper that does not point out any limitations---either the authors are over-selling or they don't fully understand DR CRAG, or both. 

**Examples**: 

- DR CRAG is identifiable in the limit of infinite data? How big is the gap between theory and reality, with finite data?
- Your experiments indicate that DR CRAG does not perform very well when there are pictures of cats in the training data. Why not? Does this suggest future research?
- Does DR CRAG require vast computational resources? Huge amounts of data? Stronger assumptions than you'd like? Does it fail to solve a closely related problem? Does it rely on a method that is hard (but separate progress is being made)?




## Some additional tips and resources

- When drafting a paper, it can help to insert a detailed sketch of a plot (axis labels, lines/points/bars, etc.) as a placeholder for the real thing. This can help you figure out exactly what experiment you need to run to generate the right plot. 
- Colors, scales, fonts, etc., matter! Your paper is already hard to understand---don't make it harder. 
- [Fundamentals of Data Visualization](https://clauswilke.com/dataviz/)
- [Trevor Campbell's talk on "How to Explain Things"](https://docs.google.com/presentation/d/13vwchlzQAZjjfiI3AiBC_kM-syI6GJKzbuZoLxgy1a4/edit?slide=id.g4fbcbb044c_0_0#slide=id.g4fbcbb044c_0_0) addresses some related things



