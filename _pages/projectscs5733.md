---
layout: page
permalink: /projectscs5733/
title: Some feasible Project Ideas, based on earlier Courses
description: CS5733 Program Synthesis, Class Project Ideas
nav: false
nav_order: 6
---

Here are some project ideas, roughly in the order of increasing difficulty / scope. For all projects that involve applying synthesis in a new domain, the *default* is to use an existing synthesis framework such as Sketch, Rosette, or PROSE, but you can also implement a synthesizer from scratch if you feel up to task. 

* Reproduce experimental results from any paper we read.
* **CEGIS:** Re-implement a symbolic program synthesizer based on a CEGIS loop. Your synthesizer must accept input in the [Sygus](http://sygus.org/) format.

* **Grammar reduction:** In the class, we talked about how a grammar can be reduced so that it doesn't generate redundant expressions in the first place. Implement a tool that generates a reduced grammar from a set of equivalences or rewrite rules. Compare it with a tool a-la Smith&Albarghouthi that checks generated programs for normality.
* **Extending Probe:** [Probe](https://cseweb.ucsd.edu/~npolikarpova/publications/oopsla20-probe.pdf) is a SyGus solver that performs weighted bottom-up search with weights learned on the fly, from partial solutions. You can consider extending Probe in several ways:
  * Add conditionals: Currently Probe has no specific optimizations for learning conditionals, hence it performs poorly on conditional-rich Euphony benchmarks. The idea would be to add EU-Solver style condition abduction to Probe.
* **Bottom-up enumeration in egg:** Bottom-up enumeration with observation equivalence reduction stores all the programs it has enumerated in program bank. It also discards observationally-equivalent terms, so there is no way to generate more than one program that satisfies all the examples. The idea of this project is to re-implement bottom-up enumeration, but store all enumerated terms in an e-graph, using the efficient [egg library](https://egraphs-good.github.io/). The main challenge is implement an operation that *incrementally* updates the e-graph once a new IO example is added (by splitting the equivalence classes and re-routing all the edges), so that enumeration does not have to start from scratch every time.

* **Extending Tree Automata based-synthesis with constraints** The FTA based synthesis, discussed in the class suffer from expressive limitations. These FTAs cannot model condtraints over trees, e.g. it is not feasible to only express terms of the form f (a, a), f ( f ( b, b), f (b, b)), etc. There is some recent work [ECTA](https://dl.acm.org/doi/abs/10.1145/3547622) in extending FTAs with such constraints. The goal of this project will be either to implement this work to develop a SAT Solver using these new FTAs. The idea is discussed in the paper. 

* **Synthesis with ASP** There is some [recent work](https://mgree.github.io/papers/2023popl_asp.pdf) on using Answer-Set Programming (ASP) to synthesize Datalog programs. The goal of this project would be to apply ASP to a different relational domain, e.g. synthesizing context-free grammars (or tree grammars).
* **Extending LEAP:** [LEAP](https://arxiv.org/abs/2306.09541) is a tool that combines an LLM with Live Programming to help programmers validate AI's code suggestions. You can consider extending LEAP in several ways:
   * Currently the programmer needs to invoke the function on a concrete input in order to see its behavior with Live Programming. You will modify LEAP to use the LLM to generate informative inputs
   * Integrate LEAP with either human-written or automatically-generated assertions/tests (perhaps following the ideas in [this paper](https://arxiv.org/pdf/2210.00848.pdf)) to filter out irrelevant suggestions
   * Different AI suggestions are often semantically similar (even if syntactically not identical). You could extend LEAP to analyze program traces in order to filter out semantically equivalent programs.

* **Top-down library learning over e-graphs** Library learning is the problem of discovering common functionality in a corpus of programs and factoring it out into library functions. [Stitch](https://arxiv.org/abs/2211.16605) is an efficient library learning tool, but it does not work over e-graphs (i.e. it does not take into account that syntactically different programs could be semantically equivalent). In this project, you will adapt Stitch to work over e-graphs. 

* **ARC:** [Abstraction and Reasoning Challenge](https://www.kaggle.com/c/abstraction-and-reasoning-challenge) is a dataset of inductive learning programs over 2D grids, designed to measure human-like intelligence. One of the most versatile ways of modeling ARC problems is using [cellular automata](https://en.wikipedia.org/wiki/Cellular_automaton) (CA). In this project you will implement an enumerative synthesizer for generating CAs that solve ARC problems.