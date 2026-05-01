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
- Local WebBGPT repository
- VS Code
- Python 3.12 environment
- GitHub repository
- Webb-specific mock data
- Domain corpus files
- Tokenizer artifacts
- Local MVP model configs
- Training and evaluation scripts

<img src="images/webbgpt-repo-overview.png">
<img src="images/webbgpt-vscode-project.png">


## Step-by-Step Process
1. **Set up the project repository**: I first organized the WebBGPT codebase inside VS Code and connected it to GitHub so that changes could be tracked cleanly. This made the project easier to manage as the number of files, configs, and experiments increased.

2. **Build the local MVP path**: Instead of trying to immediately train the full long-term model, I focused on a smaller local MVP that could run on available hardware. This made the project more testable because I could quickly change configs, rebuild data, and compare results.

3. **Prepare the Webb-specific data**: I added Webb-grounded prose and domain-specific text so the model would not only learn general language patterns, but also begin to understand Webb-style school information. This included course/catalog-style writing, advising information, and handbook/catalog distinctions.

4. **Train the raw language model**: I ran pretraining on the local MVP model and monitored loss, perplexity, and qualitative samples. The early generations were repetitive and unstable, but they helped reveal what the model was actually learning and where the setup still needed improvement.

5. **Diagnose the quality problem**: The model’s samples were worse than expected because the original setup was undertrained and the token budget was too low for the parameter count. Even when perplexity improved, the model still produced looping phrases and topic drift, which showed that raw-LM quality needed more than just a small decrease in loss.

6. **Resize the model for better iteration**: I changed the local MVP path to a smaller 22-million-parameter model so it could receive more training tokens per parameter. This made the local experiment more realistic because the model had a better chance of becoming readable before hitting hardware or time limits.

7. **Improve evaluation**: I kept the raw-LM evaluation separate from chat-style prompting so the model could be judged honestly. Instead of wrapping prompts in assistant tags, I tested generation from plain raw prefixes to see whether the pretrained model itself was becoming coherent.

8. **Plan the next phase**: The next goal is to continue improving the training data, monitor perplexity and generation quality together, and eventually use the local MVP as a foundation for a larger Webb-specific assistant.

<img src="images/webbgpt-terminal-training.png">
<img src="images/webbgpt-config-files.png">
<img src="images/webbgpt-data-folder.png">
<img src="images/webbgpt-eval-output.png">
<img src="images/webbgpt-loss-chart.png">



## Problems + Solutions
- **Undertrained model**: The first local MVP generations were weak because the model had not seen enough tokens relative to its size. The solution was to reduce the model size and increase the effective training exposure so the model could learn more from the available corpus.

- **Perplexity did not match generation quality**: Even when perplexity improved, the generated samples still had repetition and drift. The solution was to judge the model with both numerical metrics and qualitative raw-LM samples instead of relying on perplexity alone.

- **Batch size mismatch**: The training config suggested a larger global batch size, but the actual training loop used a smaller effective batch. The solution was to inspect the training code directly instead of trusting the config labels alone.

- **Too much weak or noisy data**: Some text sources did not match the Webb-specific goal or were too messy for high-quality training. The solution was to clean, reshape, and filter domain corpora so that the model saw more coherent paragraph-style training examples.

- **Chat-wrapper confusion**: Early evaluation could be misleading if the model was tested with chat formatting before it had actually been trained as a chat assistant. The solution was to evaluate it as a raw language model first, using plain text prefixes.

<img src="images/webbgpt-bad-sample-looping.png">
<img src="images/webbgpt-training-log.png">
<img src="images/webbgpt-preprocess-script.png">


## Main Takeaways  
- **A small model still needs serious data discipline**: Even a local MVP cannot become useful just by running training. The data quality, token budget, batch behavior, and evaluation setup all matter.

- **Perplexity is useful but incomplete**: Lower perplexity can show progress, but readable generation is its own test. The project needs both metrics and human inspection.

- **WebBGPT needs two paths**: The local MVP is useful for learning, debugging, and proving the pipeline. The larger long-term model is still the real vision, but it should be built only after the smaller path is stable.

- **Grounding matters more than sounding confident**: The final goal is not just to make a model that writes fluent text. It needs to answer Webb-related questions carefully, admit uncertainty, and rely on school-grounded information when possible.

<img src="images/webbgpt-before-after-samples.png">
<img src="images/webbgpt-webb-domain-corpus.png">
<img src="images/webbgpt-project-diagram.png">
<img src="images/webbgpt-github-commits.png">
  

## Reflection
WebBGPT has become a much deeper project than just “train a small AI model.” At first, it seemed like the main challenge would be getting the code to run, but the harder part has been understanding why the model behaves the way it does. When the samples looked bad, the answer was not simply that the model failed. It was that the setup, data, training budget, and evaluation method all needed to be examined together.

The project is still early, but the local MVP path has already been useful because it exposes problems quickly. A bad generation sample is frustrating, but it is also information. It shows whether the model is undertrained, whether the data is messy, whether the prompt format is wrong, or whether the model size is unrealistic for the available training budget.

The long-term goal is still to make WebBGPT into a Webb-specific assistant that can answer school-related questions in a grounded and careful way. For now, the most important step is building a clean foundation: better data, clearer configs, honest evaluation, and a local model that can show real improvement over time.
