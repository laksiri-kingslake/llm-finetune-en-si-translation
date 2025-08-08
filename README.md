# LLM Fine-tune Guide

## Virtual Environment and Dependencies

1. Create
```bash
python3 -m venv .venv
```
2. Activate
```bash
source .venv/bin/activate
```
3. Deactivate
```bash
deactivate  
```
4. Install dependencies
```bash
pip install unsloth trl peft accelerate bitsandbytes torch
```

## Fine Tuning the Model

1. Open llm-en-si-translation.ipynb in Google Colab

2. Connect a T4 runtime

3. Upload en_si_translation.json

4. Execute the notebook

5. Download the model (unsloth.Q4_K_M.gguf)

6. Download Modelfile and modify if needed

## Install Ollama

1. Download and install ollama
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

2. Start
```bash
systemctl start ollama
```

## Create an Instance of the Model and Run Using Ollama
1. Copy the model file (unsloth.Q4_K_M.gguf) and Modelfile to a directory

2. Create an instance of the model
```bash
ollama create <a-name-for-the-model> -f Modelfile
```

3. List models
```bash
ollama list
```

4. Run the model
```bash
ollama run <name-of-the-model>
```
## Create a Gradio Interface

1. Install dependencies
```bash
pip install gradio request setuptools
```

2. Run gradio app
```bash
python app-gradio.py
```

## Reference
- [EASIEST Way to Fine-Tune a LLM and Use It With Ollama](https://www.youtube.com/watch?v=pTaSDVz0gok)