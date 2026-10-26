# pro_gradu_code
Repository for notebooks used in master's thesis

The process of the experiment in the notebooks:

## 1. prompt_collection.ipynb
This notebook contains the process of creating a advice-seeking professional prompt dataset, the dataset used to examine response behavior of models in the thesis experiment. The prompts were collected from four different source datasets:
The medical prompts were collected from: https://huggingface.co/datasets/lavita/ChatDoctor-HealthCareMagic-100k
The legal prompts were collected from: https://huggingface.co/datasets/jonathanli/legal-advice-reddit
The finance prompts were collected from: https://huggingface.co/datasets/llamafactory/fiqa
The therapy/counseling prompts were collected from: https://huggingface.co/datasets/Psychotherapy-LLM/PsyCoPref
For each domain-specific dataset, a subset was selected through two steps: key-word filtering followed by random sampling 300 examples. The resulting dataset consists of 1200 advice-seeking prompts balanced across four different professional domains.
## 2. model_response.ipynb

## 3. manual_test_set.ipynb
## 4. qwen_evaluator_1st_version.ipynb
## 5. evaluator_comparison.ipynb
## 6. Qwen_evaluations.ipynb
