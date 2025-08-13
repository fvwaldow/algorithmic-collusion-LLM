# Minimum Viable Product of Fish et al. (2024)
> *Fish, S., Gonczarowski, Y. A., & Shorrer, R. I. (2024). Algorithmic collusion by large language models. arXiv preprint arXiv:2404.00806, 7.*

## Overview
This repository contains the code and output accompanying an extension of the paper "Algorithmic Collusion by Large Language Models" by Fish, Gonczarowski, and Shorer. The original study focuses on the application of algorithmic pricing agents based on Large Language Models (LLMs) and sheds light on algorithmic collusion in oligopoly settings. Specifically, the study investigates whether LLMs employ anti-competitive behavior through reward-punishment schemes.

As Fish et al.'s (2024) analysis is highly focused on detecting evidence of reward-punishment strategies, the extension addresses supracompetitive prices in non-cooperative equilibrium in the case of asymmetric firms of small- to medium-scale open-source LLMs. Accompanyed by regression analysis, a textual analysis of LLM-generated plans suggest potential price leadership strategies.

## Repository Structure
`bertrand_exp_LLM`: Jupyter notebook containing the code for LLM model selection via monopoly experiment, the main bertrand competition experiment for symmetric and asymmetric firms, and additional On-Path analysis by FE regression and textual analysis considering anticometitive strategies considering the asymmetric firm setup.

`Prompt_0`: LLM output and results of Monopoly experiment

`Prompt_1` & `Asym_1`: LLM output and results of repeated Bertrand duopoly experiment for symmetric and asymmetric firms using prompt prefix P1

`Protocol_AI_Interactions`: log of Github Copilot interactions for coding

`Technical_Note`: documentation of approach assessing design choices, limitations and extension results

## Implementation Details
Since LLMs are run locally via Ollama 0.9.1, the following models must be installed a priori:
```
gemma3:4b
mistral:7b
starling-lm:7b
falcon3:7b
granite3.3:8b
llama3.1:8b
mxbai-embed-large
```

Due to long run time of the LLM simulations, it is recommended to adjust the values of `num_session` and `num_rounds` for initial code checking. The figures showing the main results can easily be reproduced by running the respective code snippet after executing `1. Experimental Setup`. Unfortunately, GitHub does not allow files larger than 25 MB to be uploaded, therefore the chapter 'Textual Analysis' must be run in its entirely to reproduce the results.

The notebook contains all the required `pip install` commands for package installation.
