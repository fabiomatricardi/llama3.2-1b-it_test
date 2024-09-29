# llama3.2-1b-it_test
DIY benchmark testing with Llama3.2-1B-instruct and streamlit


### requirements:
```
llama-cpp-python==0.3.0
streamlit==1.38.0
tiktoken
```

## GGUF source
Model card from [Bartowski repo](https://huggingface.co/bartowski/Llama-3.2-1B-Instruct-GGUF)

filename: `Llama-3.2-1B-Instruct-Q8_0.gguf`


### Model card info
Prompt format
```
<|begin_of_text|><|start_header_id|>system<|end_header_id|>

Cutting Knowledge Date: December 2023
Today Date: 26 Jul 2024

{system_prompt}<|eot_id|><|start_header_id|>user<|end_header_id|>

{prompt}<|eot_id|><|start_header_id|>assistant<|end_header_id|>
```
N_CTX = `128k`

stops = `['<|eot_id|>']`


### to be fixed
- [ ] comments not giving error on rating `DeltaGenerator(_provided_cursor=LockedCursor(_index=3...`
- [ ] logging to be fixed


### images
to be put into `images` subfolder

### external libraries
they are in `st_promptLib.py`

### logs
they goes in the `logs` subfolder

### Main streamlit file
with `venv` activated
```
python -m streamlit run st-Llama3.2-1B-it_autotest.py
```
