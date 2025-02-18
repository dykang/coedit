# CoEdIT: Text Editing by Task-Specific Instruction Tuning

This repository provides datasets, models and code for CoEdIT the instruction-tuned text editing models, with the official implementation of the following paper:
> [CoEdIT: Text Editing by Task-Specific Instruction Tuning](URL) <br>
> [Vipul Raheja](https://github.com/vipulraheja), [Dhruv Kumar](https://github.com/ddhruvkr), [Ryan Koo](https://github.com/kooryan), and [Dongyeop Kang](https://github.com/dykang)

Our code is based on Hugging Face `transformers`.

## Installation
Coming soon. 

## Data
Coming soon.

## Code
Coming soon.

## Models

#### Model checkpoints
We have uploaded all our model checkpoints to [Hugging Face](https://huggingface.co/grammarly). 

| Model         | Params        | 
| :-------------|:-------------  |
| [CoEdIT-large](https://huggingface.co/grammarly/coedit-large)      | 770M  | 
| [CoEdIT-xl](https://huggingface.co/grammarly/coedit-xl)    | 3B  | 
| [CoEdIT-xxl](https://huggingface.co/grammarly/coedit-xxl)    | 11B  | 
| [CoEdIT-xl-composite](https://huggingface.co/grammarly/coedit-xl-composite)    | 3B  |


#### Example Usage:
You can directly load our models using [Hugging Face Transformers](https://github.com/huggingface/transformers).
```python
from transformers import AutoTokenizer, T5ForConditionalGeneration

tokenizer = AutoTokenizer.from_pretrained("grammarly/coedit-xl")
model = T5ForConditionalGeneration.from_pretrained("grammarly/coedit-xl")
input_text = 'Fix grammatical errors in this sentence: New kinds of vehicles will be invented with new technology than today.'
input_ids = tokenizer(input_text, return_tensors="pt").input_ids
outputs = model.generate(input_ids, max_length=256)
edited_text = tokenizer.decode(outputs[0], skip_special_tokens=True)[0]
```

## Citation
Coming soon.
