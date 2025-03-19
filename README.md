# Convert-Multiple-Repos
Here the code snippet is used to convert multiple repository of text dataset to just one dataset. This will help in finetuning an LLM

The text format should not contain nested jsons or nested structures.

If any of the file in github repo has a nested structure then it will show this error---- "error ArrowTypeError: Expected bytes, got a 'dict' object"----- which indicates that the Hugging Face Dataset.from_list(data_list) is receiving nested dictionaries or unexpected structures, which PyArrow (used internally by Hugging Face) cannot process directly.

PyArrow expects columnar data (i.e., every key in data_list should have a uniform data type).

To check for the proper format check my repo named ,"My-Testing-dataset-for-finetuning-LLM".
