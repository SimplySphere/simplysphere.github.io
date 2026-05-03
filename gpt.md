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
- Webb-specific grounding
- Fineweb dataset
  
<img src="images/vscode.png">
<img src="images/fineweb.png">
<img src="images/webb-specific.png">

## Step-by-Step Process
1. **Separate the levels of the project**: I first realized that this project could not be done in one go, so I divided its complexity into different levels: a quick debug to check everything worked, a full version of a Webb-specific assistant, and a smaller local minimum viable product that could be iterated one faster with splits into steps like preparing data, training a tokenizer, and running pretraining for more accessibility. Separating these levels made the project feel more manageable because I could work on the local MVP without losing sight of the larger goal.

2. **Find the data**: After separating the project into levels, I focused on finding useful training material. I needed both broad general text and Webb-specific data, so I used FineWeb-style, which had internet text from many years, and the official Webb website to link the model to the school context. 

[Fineweb](https://huggingface.co/datasets/HuggingFaceFW/fineweb)

[Webb-specific](webb.org)

3. **Learn from YouTube videos and research papers**: To learn how language models work, I used YouTube videos and other explanations to understand the basic training pipeline. I learned more about tokenizers, pretraining, model size, attention, and transformers.

- [Large Language Models explained briefly](https://www.youtube.com/watch?v=LPZh9BOjkQs&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=6): a brief explanation of what large language models are and why predicting text can create useful behavior.
- [Transformers, the tech behind LLMs | Deep Learning Chapter 5](https://www.youtube.com/watch?v=wjZofJX0v4M&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=7): an explanation of the Transformer architecture behind modern language models.
- [How might LLMs store facts | Deep Learning Chapter 7](https://www.youtube.com/watch?v=9-Jl0dxWQs8&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=9): an explanation of how facts and knowledge may be represented inside language model weights.
- [They solved AI’s memory problem!](https://www.youtube.com/watch?v=2IfAVV7ewO0&list=LL&index=15): a video on how AI systems can use memory or retrieval to work with information beyond a single prompt.
- [They solved AI hallucinations!](https://www.youtube.com/watch?v=1ONwQzauqkc): a video on the root of hallucinations within neural networks; thus, they have a way to notice when hallucinations happen to ensure reliable information.
- [The Math Needed for AI/ML (Complete Roadmap)](https://www.youtube.com/watch?v=YZOAiJmnNvc&list=LL&index=22): a roadmap of the math foundations needed to understand machine learning.

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762): the original Transformer paper that introduced the architecture behind many modern LLMs.
- [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html): a technical framework for understanding how Transformer components may form interpretable circuits.
- [Superposition Yields Robust Neural Scaling](https://arxiv.org/abs/2505.10465v4): a research paper connected to how neural networks may represent more features than they have obvious separate dimensions for; thus, LLMs are slowly reaching their limit.

4. **Create a prototype**: Once I had a better understanding of the pipeline, I created a local MVP prototype. This prototype was not meant to be the final version. Instead, it was a smaller test model that could test the basic process: prepare data, train a tokenizer, configure the model, run pretraining, and evaluate raw generation quality.

5. **Get permission from the Tech Office to use Studio B**: Training even a small language model takes time and hardware resources, so I needed to use the Studio B machine. Thus, I had to communicate my intentions and project to the Tech Office to gain access, which tested my ability to interact with others in tech spaces.

6. **Iterate slowly**: After getting the project running, the process became a slow iteration. I looked at training logs, checked perplexity, reviwed bad generation samples, adjusted configs, cleaned data, and tried to understand why the model behaved as it did. The project is still in early development, but each cycle provides more information about what needs improvement next.

<img src="images/webbgpt-levels.png">

<div style="width: 90%; height: 700px; border: 1px solid #ccc; border-radius: 8px; overflow: hidden; margin: 20px 0;">
  <iframe 
    src="files/studio-b-request.pdf" 
    width="100%" 
    height="100%" 
    style="border: none;">
  </iframe>
</div>

<div style="width: 90%; height: 700px; border: 1px solid #ccc; border-radius: 8px; overflow: hidden; margin: 20px 0;">
  <iframe 
    src="files/webbgpt-final-eval.pdf" 
    width="100%" 
    height="100%" 
    style="border: none;">
  </iframe>
</div>

## Problems + Solutions
- **Large training runs are expensive**: Training a serious language model can take a lot of compute, so the project uses smaller local profiles first. The `debug` profile proves the pipeline works quickly, while `local-mvp` gives a better local test without jumping straight to massive models.

- **Generic answers are not enough**: A normal model may give vague or incorrect Webb answers. The solution was to add grounding, Webb-specific datasets, source policies, and evaluation prompts so answers can be checked against actual project data.

- **Quality is hard to measure**: A model can appear to work in a few examples but still fail on hidden cases. WebbGPT handles this by using evaluation files, validation data, test cases, and experiment notes that track problems like topic drift, semantic loops, and weak catalog accuracy.

<div style="width: 90%; height: 700px; border: 1px solid #ccc; border-radius: 8px; overflow: hidden; margin: 20px 0;">
  <iframe 
    src="files/webbgpt-training.pdf" 
    width="100%" 
    height="100%" 
    style="border: none;">
  </iframe>
</div>

<source src="images/webbgpt-sample.MOV" type="video/mp4">

## Main Takeaways
- **A chatbot is more than a model**: WebbGPT showed that the model itself is only one part of the system. The data pipeline, configs, grounding database, evaluations, export step, and serving app are all necessary for the assistant to actually work.

- **Local testing matters**: Having `debug` and `local-mvp` profiles makes the project easier to develop because changes can be tested before running larger experiments.

- **Grounding improves trust**: Connecting answers to Webb data and citations makes the assistant more useful because users can see where information came from instead of blindly trusting generated text.

<img src="images/webbgpt-status-page.png">
<img src="images/webbgpt-tests.png">

## Reflection
WebbGPT is a challenging project because it combines machine learning, data preparation, backend serving, evaluation, and school-specific knowledge. It is not just about making a chatbot respond; it is about making the entire system reproducible and trustworthy.

The most important progress so far is that the project has a clear structure. There are configs for different run sizes, Webb data sources, tests, evaluation prompts, and a browser playground. The next step is continuing to improve answer quality, reduce drift, and make the local assistant more reliable when answering Webb-specific questions.
