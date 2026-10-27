# pro_gradu_code
Repository for notebooks used in master's thesis

The process of the experiment in the notebooks:

## 1. prompt_collection.ipynb
This notebook contains the process of creating an advice-seeking professional prompt dataset, the dataset used to examine response behavior of models in the thesis experiment. The prompts were collected from four different source datasets:

The medical prompts were collected from: https://huggingface.co/datasets/lavita/ChatDoctor-HealthCareMagic-100k
The legal prompts were collected from: https://huggingface.co/datasets/jonathanli/legal-advice-reddit
The finance prompts were collected from: https://huggingface.co/datasets/llamafactory/fiqa
The therapy/counseling prompts were collected from: https://huggingface.co/datasets/Psychotherapy-LLM/PsyCoPref

For each domain-specific dataset, a subset was selected through two steps: key-word filtering followed by random sampling 300 examples. The resulting dataset consists of 1200 advice-seeking prompts balanced across four different professional domains.
## 2. model_response.ipynb
This notebook contains the process of collecting model responses to the prompts of the prompt dataset. The two models which responses were collected were GPT-4o mini (snapshot gpt-4o-mini-2024-07-18) and 8-billion parameter version of the Llama 3.1 Instruct (with 4-bit quantization). After the response generation process, 2 400 responses were obtained for evaluating model response behavior, with each of the two models generating 1 200 responses to the advice-seeking prompt dataset of 1 200 examples.
## 3. manual_test_set.ipynb
This notebook contains the creation of the manually classified test set. 120 GPT responses and 120 Llama responses were manually classified, with the 120 examples balanced across the professional domains (30 examples from each domain). 
## 4. qwen_evaluator_1st_version.ipynb
This notebook contains the first version of the system prompt, where the LLM-as-a-judge was given instructions on classifying the responses but wasn't instructed to explain its decision. This version was not used for the final results of the thesis because the second version had better performance.
## 5. evaluator_comparison.ipynb
This notebook contains the comparison of the first and second system prompting methods for the LLM-as-a-judge. The results of the final LLM-as-a-judge's performance (accuracies, confusion matrices) in the thesis come from this notebook.
## 6. Qwen_evaluations.ipynb
This notebook contains the final chosen method for prompting the LLM-as-a-judge and the final process of collecting model response evaluations. In the second part of the notebook are the results and visualizations of model response evaluations referenced in the thesis "Results" section.
## 7. manual_assesment.ipynb
This notebook contains process of collecting the subsets used for the manual assesment part of the thesis "Results" section
