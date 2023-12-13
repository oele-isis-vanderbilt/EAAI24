# A Chain-of-Thought Prompting Approach with LLMs for Evaluating Students’ Formative Assessment Responses in Science
## Clayton Cohn, Nicole Hutchins, Tuan Le, Gautam Biswas

### Abstract
This paper examines the use of LLMs to support the grading and explanation of short-answer formative assessments in K-12 science topics. While significant work has been done on programmatically scoring well-structured student assessments in math and computer science, many of these approaches produce a numerical score and stop short of providing teachers and students with explanations for the assigned scores. In this paper, we investigate few-shot, in-context learning with chain-of-thought reasoning and active learning using GPT-4 for automated assessment of students' answers in a middle school Earth Science curriculum. Our findings from this human-in-the-loop approach demonstrate success in scoring formative assessment responses and in providing meaningful explanations for the assigned score. We then perform a systematic analysis of the advantages and limitations of our approach. This research provides insight into how we can use human-in-the-loop methods for the continual improvement of automated grading for open-ended science assessments.

### Supplemental Materials
Our Supplemental Materials include additional information that is omitted from the manuscript for brevity but informative to researchers interested in the process details and method application. Additionally, this information is provided for the purposes of enhancing reproducibility and aiding researchers wishing to apply our method to their own task, domain, or dataset. We include:
1. **Curriculum Context**. The formative assessment questions and corresponding rubrics we used for this work.
2. **Prompts**. The initial prompts used for our Chain-of-Thought Prompting + Active Learning approach (one prompt for each formative assessment question). These prompts include the initial few-shot examples selected as a result of the IRR process (Response Scoring), but they do not include the additional few-shot instances selected during active learning.
3. **Method Application Details**. For each formative assessment question, we detail our method in a step-by-step fashion, enumerating each step of the process with the specific details that guided our prompt generation and refinement.

### Code & Data
We have included Python code that can be used to both prompt GPT-4 through the OpenAI API and conduct analysis on the model generations. Code files are heavily commented in-line and require certain variables be changed (e.g. save/load paths, Open AI API key, etc.). Along with the code is a data sample that can be used to test the scripts and understand the proper formatting. All included files are enumerated and explained below.

1. **generations.ipynb** — code to pass prompts to GPT-4 via Open AI API call, receive responses (model generations), and save the generations.
2. **analysis.ipynb** — code to parse the generations (and extract model scores), conduct the analysis, and save the model scores for further analysis.
3. **Q3_ANON_SAMPLE.csv** — an anonymized sample of students’ formative assessment responses for Q3. Importantly, this is just a sample subset of the data, so the results may not reflect the same Q3 results reported in the manuscript. Our full dataset can be made available upon request.
4. **DEMO_PROMPT.txt** — Our Q3 prompt for CoT (prior to active learning) that was used for this appendix.
5. **DEMO_GENERATIONS.csv** — The file containing the model generations (alongside human scores and other information for each instance) from the generations.ipynb file.
6. **DEMO_FULL_SCORES.csv** — DEMO_GENERATIONS.csv instances with full model scores appended. This file can be used to conduct further analysis on the model scores and explanations.

For any questions, please email Clayton Cohn at clayton.a.cohn@vanderbilt.edu.
