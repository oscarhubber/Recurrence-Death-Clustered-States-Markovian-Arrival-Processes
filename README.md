The postmortem branch was created after the defense of this Master's Thesis. Its purpose is to neatly present to future viewers the code that I developed for the project. Bear in mind, the main objective of this project was to obtain new results and insights for the novel RD CS-MAP mathematical model. The evaluation was based exclusively on the contents and presentation of the Thesis report and the Thesis defense, NOT on the codebase (I uploaded it anyway upon request of my advisor). As a result, the original codebase was much messier than the one present here.

In this branch, compilation results have been excluded from the notebooks, so that they can be comfortably read within GitHub. The most important notebooks are the following two:

· "PROGRAMAS_CSMAPS_V10.ipynb" was the main notebook where I began developing my codebase, and so it contains a little bit of everything. It consists of the following sections:
  1. In the first two sections, I imported libraries and developed a common data preprocessing procedure for the real-life datasets.
  2. In "Extracting empirical statistics from datasets", I developed functions that extract relevant empirical statistics from lifeline datasets. Such statistics are defined for the number of recurrences variable, for the inter-event times, and for the time of death.
  3. In "CS-MAP Theoretical Formulas", I developed functions that compute relevant statistics from the CS-MAP mathematical model. They are analogues to their empirical counterparts.
  4. In "Simulating CS-MAPs" section, I developed a function that performs a simulation of the CS-MAP model, similar to a continuous-time Markov chain.
  5. In "CS-MAP Reverse Engineering" section, I developed a function that randomly samples CS-MAP model parameters, and performed statistical inference using it, upon request of my advisor.
  6. In "Simulating MAPs" section, I developed a function that performs a simulation of the MAP model, a simpler model than the objective model of my thesis. This section exists for generating images for my report's preliminaries.

· "PRUEBAS_FINALES_V10.ipynb" was the final notebook where I synthesised the core results from the previous notebook (i.e. aggregated all of the relevant functions). My advisors requested me that I move on from performing inference over parameters, and that I needed to develop an optimisation procedure for fitting CS-MAP model parameters (gradient descent based on a penalised loglikelihood metric) into datasets. It consists of the following sections:
  1. In "0. Main setup", I recovered every single function that I was going to need for the optimisation procedure, and I also developed the optimisation procedure functions themselves.
  2. In "1. EXPERIMENT 1 - Uncensored, simulated sample", I began by testing the optimisation procedure on self-generated, uncensored samples.
  3. In "2. EXPERIMENT 2 - Censored, simulated sample", I tested the optimisation procedure on self-generated, censored samples. Censorship was dealt with by means of two different ad-hoc methods, and results were carried out for both methods.
  4. In "3. EXPERIMENT 3 - Real sample", I finally ran the optimisation procedure on the real life datasets, using both methods of dealing with censorship as well.
