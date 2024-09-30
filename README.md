# RBYF is here: Revised Benchmarks with You as a Feedback

AKA: llama3.2-1b-it_test - DIY benchmark testing with Llama3.2-1B-instruct and streamlit

### Llama3.2-1B-instruct is good… but not enough!
<img src='https://github.com/fabiomatricardi/llama3.2-1b-it_test/raw/main/Llama3.2-1b_instruct_ToC_eval.png' width=900>
<br><br>

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



### images
to be put into `images` subfolder

### external libraries
they are in `st_promptLib.py`
<br><br>
For evaluation we are going to use the following Qualitative Matrix:
<br><br>
<img src='https://github.com/fabiomatricardi/llama3.2-1b-it_test/raw/main/evaluationMatrix_long.png' width=900>
<br><br>

### logs
they goes in the `logs` subfolder


## Textual Interface Auto Test with Revised Benchmarks with You as a Feedback
with `venv` activated
```
python main.py
```
If you want to use GPU (like with BVulkan support or Nvidia if you have it...)
```
python main.py -g
```
You will get something like this:<br><br>
<img src='https://github.com/fabiomatricardi/llama3.2-1b-it_test/raw/main/llama3.2_1btest.gif' width=900>
<br><br>




### Main streamlit file
with `venv` activated
```
python -m streamlit run st-Llama3.2-1B-it_autotest.py
```

### to be fixed
- [ ] comments not giving error on rating `DeltaGenerator(_provided_cursor=LockedCursor(_index=3...`
- [ ] logging to be fixed


