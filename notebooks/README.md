# Notebooks

These notebooks are an opinionated way of splitting long-form 
speech into text-aligned segments.

Launch the Jupyter Notebook UI with:
```commandline
poetry run jupyter notebook
```

### collect_data.ipynb
processes a long-form speech corpus into a specific directory 
structure. (this is a dependency for the next step)

### ctc_segmentation.ipynb
runs CTC segmentation on the long audios using models from the 
NeMo toolkit

### upload_dataset.ipynb
formats the aligned audio and text segments, and upload to HF Hub

---
The remaining notebooks will fine-tune a Whisper 
variation on the dataset you just created. Nothing new 
here - HuggingFace Hub makes everything easy to run, 
given you have access to GPU compute.

### whisper_tuning.ipynb
fine-tuning of a pre-trained Whisper checkpoint on our train dataset

### whisper_inference.ipynb
inference and evaluation of fine-tuned Whisper checkpoint on our test dataset
