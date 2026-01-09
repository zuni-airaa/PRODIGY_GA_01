[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zuni-airaa/PRODIGY_GA_01/blob/main/notebooks/PRODIGY_GA_01.ipynb)

# PRODIGY_GA_01

##  Project Overview
This project demonstrates fine-tuning **GPT-2**, a transformer-based language model developed by OpenAI, to generate coherent and contextually relevant text. By training on a custom dataset, the model learns to mimic the style and structure of the training data.

##  Features
- Fine-tuning GPT-2 using HuggingFace Transformers
- Custom dataset integration
- Text generation with prompts
- Example outputs showcasing generated text

##  Repository Structure
- `notebooks/` → Colab notebook for training and generation
- `data/` → Sample dataset (if provided)
- `results/` → Generated text samples
- `README.md` → Project documentation
- `requirements.txt` → Dependencies

##  Setup
Install dependencies:
```bash
pip install transformers datasets torch
```

Run the notebook in Google Colab or locally to fine-tune GPT-2.

##  References
- HuggingFace Blog: [How to generate text](https://huggingface.co/blog/how-to-generate)
- Colab Notebook: [Text generation tutorial](https://colab.research.google.com/drive/15qBZx5y9rdaQSyWpsreMDnTiZ5IlN0zD?usp=sharing)

##  Example Usage
```python
from transformers import GPT2Tokenizer, GPT2LMHeadModel

tokenizer = GPT2Tokenizer.from_pretrained("gpt2")
model = GPT2LMHeadModel.from_pretrained("gpt2")

prompt = "The future of AI is"
inputs = tokenizer.encode(prompt, return_tensors="pt")
outputs = model.generate(inputs, max_length=50, temperature=0.7, top_p=0.9, do_sample=True)

print(tokenizer.decode(outputs[0], skip_special_tokens=True))
```

##  Results

Here are some example outputs generated after fine‑tuning GPT‑2:

**Prompt:**  
`The future of AI is.`

**Generated Output:**  
`The future of AI is filled with opportunities, where machines assist humans in solving complex problems, creating new ideas, and inspiring innovation across industries.`

---

**Prompt:**  
`Self‑motivation comes from.`

**Generated Output:**  
`Self‑motivation comes from believing in your own potential, setting clear goals, and taking small steps every day toward progress.`

---

Sample outputs are stored in the `results/` folder for reference.

```
##  Repository Structure (Task‑01)
PRODIGY_GA_01/
├── data/
│   ├── train.txt
│   └── samples.txt
├── results/
├── README.md
├── requirements.txt
├── notebooks/
│   └── PRODIGY_GA_01.ipynb
├── prodigy_ga_01.py
└── README.md



