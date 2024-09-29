# llama3.2-1b-it_test
DIY benchmark testing with Llama3.2-1B-instruct and streamlit


### requirements:
```
llama-cpp-python==0.3.0
streamlit==1.38.0
tiktoken
```

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
