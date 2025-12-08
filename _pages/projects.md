---
layout: page
title: projects
permalink: /projects/
description: 
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->




## Representative Research Projects.
Our group is involved in several interesting projects across **Programming Languages, Type systems, Program Verification and Synthesis and Neurosymbolic programming.** Below, I list some of the these:

#### Formal Methdos for Verification and Synthesis:
This umbrella project aims to make fundamental contributions towards using Formal Methods (e.g. Refinement Types) for program verification and synthesis, to aid programers to write correct programs. If you are new to Formal Methods, Galois Inc. gives a very nice recent intro on [**What are Formal Methods?**](https://www.galois.com/what-are-formal-methods)


We are developing novel type systems and domain-specific languages aimed at:

 - Verify under-approximate properties of programs using [Coverage Types](https://aegis-iisc.github.io/assets/pdf/poirotpreprint.pdf).

 - Verifying properties of higher-order parser combinators using [Morpheus](https://arxiv.org/abs/2305.07901v1).

 - Scalable component-based program synthesis over refinement-typed libraries using Novel tree automata representation [Hegel](https://arxiv.org/abs/2508.14614).

 - Synthesizing coverage complete programs using Coverage Types [Cobb](https://arxiv.org/abs/2504.06421).


####  Neurosymbolic Programing/ Neurosymbolic AI:
[**Neurosymbolic AI**](https://neurips.cc/virtual/2022/55804) and [**Neurosymbolic AI**](https://www.centaurinstitute.org/education) are two closely related, promising  areas at the intersection of Programming Languages and AI/ML. We have several projects in this direction combining the power of Formal Methods/PL with the immense potentials of AI/ML.

The common theme in this thread is towards developing ovel NeuroSymbolic techniques and tools to address the limitations of both Neural and Symbolic approaches. 

We are working towards expanding the state-of-the-art in program synthesis, allowing synthesis of efficient, robust, and verified programs for challenging low-level, safety-critical programming tasks.


#### Neurosymbolic Program Synthesis in X.
This project aims to solve challenging and error-prone programming tasks in various domains using program synthesis. Two of the main works in this area include:

 - DUNE: Multi-Modal, NeuroSymbolic Synthesis for Automatic Data Transformation:
 - TANTRA: Automated generation of correct low-level network configuration files from high-level network properties.

Here is a detailed [list (a bit dated)](https://docs.google.com/spreadsheets/d/1F0MH949En1wn-iCDS6dunkIs8YdwxZjLkXsY7Xy2iro/edit?usp=sharing) curated by [Prof. Loris D'Antoni](https://cseweb.ucsd.edu/~ldantoni/) application of Program Synthesis in different domains.



####  Trustworthy Concurrency:
Programming and reasoning about concurrent programs is notoriously challenging while, unfixing bugs in them is even harder.
we aim to develop (semi)automated and scalable reasoning methods and tools to aid programmers write correct concurrent programs, particulalrly in the domain of Concurret programs running on Hardward and compilers allowing weaker memory models that the standard sequential consistency.
