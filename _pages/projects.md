---
layout: page
title: projects
permalink: /projects/
description: projects
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->

Our group is involved in several interesting projects across **Programming Languages, Type systems, Program Verification and Synthesis, and Neurosymbolic programming/AI.** Below, I list some of these:

#### Formal Methods for Verification and Synthesis:

This umbrella project aims to make fundamental contributions to the use of Formal Methods (e.g., Refinement Types) for program verification and synthesis, to aid programmers write correct/safe programs. If you are new to Formal Methods, Galois gives a very nice recent intro on [What are Formal Methods?](https://www.galois.com/what-are-formal-methods)


We are developing novel type systems and domain-specific languages aimed at:

 - Verifying under-approximate properties of programs using [Coverage Types](https://aegis-iisc.github.io/assets/pdf/poirotpreprint.pdf).

 - Verifying properties of higher-order parser combinators using [Morpheus](https://arxiv.org/abs/2305.07901v1).

 - Scalable component-based program synthesis over refinement-typed libraries using Novel tree automata representation [Hegel](https://arxiv.org/abs/2508.14614).

 - Synthesizing coverage-complete programs using Coverage Types [Cobb](https://arxiv.org/abs/2504.06421).


####  Neurosymbolic Programming/ Neurosymbolic AI:

[Neurosymbolic Programming](https://neurips.cc/virtual/2022/55804) and [Neurosymbolic AI](https://www.centaurinstitute.org/education) are two closely related, promising areas at the intersection of Programming Languages and AI/ML.We have several on-going works in this direction combining the power of Formal Methods/PL with the immense potential of AI/ML.
The common theme in these works is the development of novel NeuroSymbolic techniques and tools to address the limitations of both Neural (AI/ML based) and Symbolic(PL/Formal Method based) approaches. 

We are working towards advancing the state of the art in program synthesis, enabling the synthesis of efficient, robust, and verified programs for challenging low-level, safety-critical programming tasks.


#### Neurosymbolic Program Synthesis for X:

This project aims to solve challenging, error-prone programming tasks across various domains using program synthesis. Two of the main works in this area include:

 - DUNE: Multi-Modal, NeuroSymbolic Synthesis for Automatic Data Transformation.
 - TANTRA: Automated generation of correct low-level network configurations.

To understand the flavor of things here, this is a detailed [list (a bit dated)](https://docs.google.com/spreadsheets/d/1F0MH949En1wn-iCDS6dunkIs8YdwxZjLkXsY7Xy2iro/edit?usp=sharing) curated by [Prof. Loris D'Antoni](https://cseweb.ucsd.edu/~ldantoni/) on the application of Program Synthesis in different domains.



####  Trustworthy Concurrency:

Programming and reasoning about concurrent programs is notoriously challenging, while fixing bugs in them is even harder.
We aim to develop (semi)automated and scalable reasoning methods and tools to aid programmers in writing correct concurrent programs, particularly in domains where concurrent programs run on hardware and compilers that support weaker memory models than the standard sequential consistency.
