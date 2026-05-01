---
title: WebbGPT 0.1
layout: default
---

# WebbGPT 0.1

## Motivating Questions + Objective
- How can I build a **language model** that learns to generate readable text?
- How can I create a **local version** of the **larger long-term model**?
- How can I make a Webb-specific assistant that answers questions using **school-grounded information**?

**Objective:** To build a rudimentary large language model, **WebbGPT**, a Webb-specific language model project that can respond with answers built for the Webb community.

## Materials
- VS Code
- Webb-specific data
- Domain corpus files
- Tokenizer artifacts
  
<img src="images/webbgpt-repo.png">
<img src="images/webbgpt-configs.png">

## Step-by-Step Process
1. **Define the goal**: The project started with the idea of making a Webb-focused assistant, not just a general chatbot. The goal was to create a system that could understand Webb-related information and answer questions in a more controlled, testable way.

2. **Organize the pipeline**: WebbGPT was built as a Python CLI with several stages: building a tokenizer corpus, training a tokenizer, preparing data, pretraining, continued pretraining, SFT, DPO, evaluation, export, and serving.

3. **Create local development profiles**: Instead of making every run huge and expensive, the project includes profiles like `debug` and `local-mvp`. The debug profile is for quick smoke tests, while `local-mvp` is the main local-development path.

4. **Prepare Webb-specific data**: The project includes Webb mock pages, handbook-style information, catalog data, advising data, and local training files. This lets the assistant learn from school-specific context while still keeping the workflow testable offline.

5. **Add grounding**: WebbGPT does not only rely on what the model memorized. It can sync Webb data into a local grounding database, retrieve relevant information, and attach citations to answers.

6. **Build a playground**: The final system can be served with FastAPI and opened in a browser. This makes it possible to test the assistant directly instead of only checking terminal outputs.

7. **Evaluate quality**: The project includes evaluation files for catalog questions, Webb admissions, athletics, student life, faculty, handbook information, and general assistant behavior. These tests help reveal drift, missing information, and weak answer quality.

<img src="images/webbgpt-cli.png">
<img src="images/webbgpt-data-folder.png">
<img src="images/webbgpt-playground.png">

## Problems + Solutions
- **Large training runs are expensive**: Training a serious language model can take a lot of compute, so the project uses smaller local profiles first. The `debug` profile proves the pipeline works quickly, while `local-mvp` gives a better local test without jumping straight to massive models.

- **Generic answers are not enough**: A normal model may give vague or incorrect Webb answers. The solution was to add grounding, Webb-specific datasets, source policies, and evaluation prompts so answers can be checked against actual project data.

- **Quality is hard to measure**: A model can appear to work in a few examples but still fail on hidden cases. WebbGPT handles this by using evaluation files, validation data, test cases, and experiment notes that track problems like topic drift, semantic loops, and weak catalog accuracy.

<img src="images/webbgpt-eval-files.png">
<img src="images/webbgpt-grounding.png">

## Main Takeaways
- **A chatbot is more than a model**: WebbGPT showed that the model itself is only one part of the system. The data pipeline, configs, grounding database, evaluations, export step, and serving app are all necessary for the assistant to actually work.

- **Local testing matters**: Having `debug` and `local-mvp` profiles makes the project easier to develop because changes can be tested before running larger experiments.

- **Grounding improves trust**: Connecting answers to Webb data and citations makes the assistant more useful because users can see where information came from instead of blindly trusting generated text.

<img src="images/webbgpt-status-page.png">
<img src="images/webbgpt-tests.png">

## Reflection
WebbGPT is a challenging project because it combines machine learning, data preparation, backend serving, evaluation, and school-specific knowledge. It is not just about making a chatbot respond; it is about making the entire system reproducible and trustworthy.

The most important progress so far is that the project has a clear structure. There are configs for different run sizes, Webb data sources, tests, evaluation prompts, and a browser playground. The next step is continuing to improve answer quality, reduce drift, and make the local assistant more reliable when answering Webb-specific questions.
