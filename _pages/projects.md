---
layout: page
title: projects
permalink: /projects/
description: Research projects in Programming Languages, Formal Methods, and Neurosymbolic AI.
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

Our group is involved in several interesting projects across **Programming Languages, Type systems, Program Verification and Synthesis, and Neurosymbolic programming/AI.** Below, I list some of these:

<style>
  .project-container {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    margin-top: 2rem;
  }
  .custom-project-card {
    display: flex;
    flex-direction: row;
    background: var(--global-bg-color);
    border-radius: 12px;
    border: 1px solid var(--global-divider-color);
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .custom-project-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 25px rgba(0,0,0,0.1);
  }
  .card-img-container {
    width: 35%;
    min-width: 250px;
    background-color: var(--global-code-bg-color);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }
  .card-img-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .card-content {
    padding: 1.5rem;
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .card-tags {
    margin-bottom: 0.75rem;
  }
  .card-tag {
    display: inline-block;
    padding: 0.2rem 0.6rem;
    background: var(--global-theme-color);
    color: var(--global-bg-color);
    border-radius: 4px;
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    margin-right: 0.5rem;
    margin-bottom: 0.5rem;
    opacity: 0.85;
  }
  .card-content h3 {
    margin-top: 0;
    margin-bottom: 1rem;
    font-size: 1.5rem;
    color: var(--global-text-color);
  }
  .card-content p {
    font-size: 0.95rem;
    line-height: 1.6;
    margin-bottom: 1rem;
    color: var(--global-text-color-light);
  }
  .card-content ul {
    margin: 0;
    padding-left: 1.2rem;
    font-size: 0.9rem;
  }
  .card-content li {
    margin-bottom: 0.3rem;
  }

  /* Expandable section styles */
  .project-details {
    margin-top: 0.25rem;
  }
  .project-details summary {
    cursor: pointer;
    font-weight: 600;
    font-size: 0.9rem;
    color: var(--global-theme-color);
    user-select: none;
    outline: none;
    margin-bottom: 0.5rem;
  }
  .project-details summary:hover {
    text-decoration: underline;
  }

  /* Dark mode adjustments using alfolio's native variables */
  html[data-theme='dark'] .custom-project-card {
    box-shadow: 0 4px 15px rgba(255,255,255,0.02);
  }
  html[data-theme='dark'] .custom-project-card:hover {
    box-shadow: 0 12px 25px rgba(255,255,255,0.05);
  }

  @media (max-width: 768px) {
    .custom-project-card { flex-direction: column; }
    .card-img-container { width: 100%; height: 200px; min-width: unset; }
  }
</style>

<div class="project-container">

  <!-- Section 1: Formal Methods -->
  <div class="custom-project-card">
    <div class="card-img-container">
      <img src="{{ '/assets/img/fm-project.png' | relative_url }}" alt="Formal Methods Verification" onerror="this.src='https://placehold.co/600x400?text=Formal+Methods'">
    </div>
    <div class="card-content">
      <div class="card-tags">
        <span class="card-tag">Formal Methods</span>
        <span class="card-tag">Lean</span>
        <span class="card-tag">Refinement Types</span>
        <span class="card-tag">Coverage Types</span>
      </div>
      <h3>Formal Methods for Verification and Synthesis</h3>
      <p>This umbrella project aims to make fundamental contributions to the use of Formal Methods (e.g., Refinement Types) to aid programmers in writing correct, safe and coverage complete programs.</p>
      <ul>
        <li><a href="https://aegis-iisc.github.io/assets/pdf/poirotpreprint.pdf">Coverage Types</a>: Under-approximate properties.</li>
        <li><a href="https://arxiv.org/abs/2305.07901v1">Morpheus</a>: Higher-order parser combinators.</li>
        <li><a href="https://arxiv.org/abs/2508.14614">Hegel</a>: Novel tree automata for synthesis.</li>
        <li><b>Lean</b>: Formal Verification.</li>
      </ul>
    </div>
  </div>

  <!-- Section 2: Trustworthy AI -->
  <div class="custom-project-card">
    <div class="card-img-container">
      <img src="{{ '/assets/img/ai-guardrails-project.png' | relative_url }}" alt="Trustworthy AI" onerror="this.src='https://placehold.co/600x400?text=Trustworthy+AI'">
    </div>
    <div class="card-content">
      <div class="card-tags">
        <span class="card-tag">Trustworthy AI</span>
        <span class="card-tag">Neurosymbolic AI</span>
        <span class="card-tag">Formal Verification</span>
        <span class="card-tag">Guardrailing</span>
      </div>
      <h3>Trustworthy AI: Guardrailing & Neuro-Formal Methods</h3>
      <details class="project-details">
        <summary>Read full project overview</summary>
        <p>Bridging the gap between AI/ML and Formal Verification, this project introduces a neuro-symbolic/neuro formal framework that uses formal methods to mathematically guardrail AI systems. By integrating neural architectures (LLMs in particular) with theorem provers like Lean, automated SMT solvers, and symbolic reasoning engines, the system replaces soft probabilistic guardrails with provably correct runtime constraints. This hybrid pipeline continuously validates neural outputs against formally defined safety specifications, effectively preventing hallucinations, logical contradictions, and policy violations in high-stakes domains. Ultimately, it provides a deterministic, mathematically sound foundation for deploying trustworthy AI where empirical evaluation alone is insufficient.</p>
      </details>
    </div>
  </div>

  <!-- Section 3: Symbolic and Neurosymbolic Program Synthesis -->
  <div class="custom-project-card">
    <div class="card-img-container">
      <img src="{{ '/assets/img/sync-project.png' | relative_url }}" alt="Program Synthesis for X" onerror="this.src='https://placehold.co/600x400?text=Synthesis+for+X'">
    </div>
    <div class="card-content">
      <div class="card-tags">
        <span class="card-tag">Synthesis for Networking</span>
        <span class="card-tag">Synthesis for Data Transform</span>
      </div>
      <h3>Symbolic and Neurosymbolic Program Synthesis</h3>
      <p>Solving challenging, error-prone programming tasks across various domains using verified program synthesis using a combination of PL and AI/ML techniques.</p>
      <ul>
        <li><b>DUNE</b>: NeuroSymbolic Synthesis for Automatic Data Transformation.</li>
        <li><b>TANTRA</b>: Correct low-level network configurations.</li>
        <li>Review the <a href="https://docs.google.com/spreadsheets/d/1F0MH949En1wn-iCDS6dunkIs8YdwxZjLkXsY7Xy2iro/edit?usp=sharing">Curated List</a> of synthesis applications.</li>
      </ul>
    </div>
  </div>

  <!-- Section 4: Concurrency -->
  <div class="custom-project-card">
    <div class="card-img-container">
      <img src="{{ '/assets/img/con-project.png' | relative_url }}" alt="Trustworthy Concurrency" onerror="this.src='https://placehold.co/600x400?text=Trustworthy+Concurrency'">
    </div>
    <div class="card-content">
      <div class="card-tags">
        <span class="card-tag">Parallelism</span>
        <span class="card-tag">Hardware</span>
      </div>
      <h3>Trustworthy Concurrency</h3>
      <p>Programming and reasoning about concurrent programs is notoriously challenging. We develop scalable reasoning methods for hardware and compilers that support weaker memory models than sequential consistency.</p>
    </div>
  </div>

</div>