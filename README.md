<div align="center">

<img src="manga-banner-top.png" alt="BYTE Manga AI banner" width="100%">

<br>

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Qwen2.5--VL-Model-8A2BE2?style=for-the-badge&logoColor=white"">
<img src="https://img.shields.io/badge/Google_Colab-GPU-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white">

</div>

---
# BYTE Applied ML — Manga Task

*Turning manga page images into structured text predictions.*

## Project Overview

This repository contains my notebook and experiment notes for the BYTE Applied ML Manga Task. The goal is to process manga page images and produce structured text predictions in JSONL format.

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Transformers](https://img.shields.io/badge/Transformers-Model_Inference-8A2BE2?style=flat-square)
![Google Colab](https://img.shields.io/badge/Google_Colab-Notebook-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)

</div>

## Model

- Model: Qwen/Qwen2.5-VL-3B-Instruct
- Inference environment: Google Colab
- GPU used: NVIDIA Tesla T4
- Model loading: 4-bit quantization
<img align="right" src="manga-banner-1-side.png" alt="BYTE Manga AI banner" width="20%">
&nbsp;



<img src="manga-banner-1.png" alt="BYTE Manga AI banner" width="20%">



- `manga_inference_clean.ipynb` — notebook for running inference and generating predictions.
- `experiments.md` — notes and preliminary results from prompt experiments.
- `requirements.txt` — Python package dependencies. 

&nbsp;

<img src="manga-banner-2.png" alt="BYTE Manga AI banner" width="20%">



1. Open `manga_inference_clean.ipynb` in Google Colab.
2. Make sure the task dataset is available at the path expected by the notebook.
3. Enable a GPU runtime in Colab.
4. Run the notebook cells in order.
5. The notebook generates JSONL predictions for the test sequences and checks the output structure.

The dataset should contain the development and test folders, along with the task's provided supporting files.

&nbsp;

<img align="right" src="manga-banner-3-side.png" alt="BYTE Manga AI banner" width="20%">
<img src="manga-banner-3.png" alt="BYTE Manga AI banner" width="20%">



Preliminary prompt and output-format experiments are documented in `experiments.md`. These experiments used only three pilot sequences, so the results are limited and should not be treated as a reliable estimate of overall performance.

<br>

<img src="manga-banner-4.png" alt="BYTE Manga AI banner" width="20%">


- The pilot experiments were conducted on a small sample.
- The final test predictions use `UNKNOWN` for speaker labels.
- Valid output structure does not guarantee high prediction accuracy.
- The notebook performs inference; it does not represent a newly trained model or newly trained model weights.

<br>


<img src="manga-banner-bottom.png" alt="BYTE Manga AI banner" width="100%">
<br>
<br>
<img src="manga-banner-5.png" alt="BYTE Manga AI banner" width="40%">



<img src="manga-banner-5a.png" alt="BYTE Manga AI banner" width="20%">


This screenshot shows the dataset path being detected and CUDA availability checked.

![Dataset and GPU check](screenshots/dataset-check.png)

<img src="manga-banner-5b.png" alt="BYTE Manga AI banner" width="20%">




The notebook installs the Python packages needed for inference.

![Dependency installation](screenshots/dependencies.png)

![Dependency installation](screenshots/dependencies2.png)

<img src="manga-banner-5c.png" alt="BYTE Manga AI banner" width="20%">


Qwen2.5-VL-3B-Instruct loaded successfully in the Colab Tesla T4 environment.

![Model loaded](screenshots/model-loaded.png)

<img src="manga-banner-5d.png" alt="BYTE Manga AI banner" width="20%">



The notebook processes the three pages of each test sequence and saves
the generated predictions in JSONL format.

![Test prediction generation](screenshots/predictions.png)

![Test prediction generation](screenshots/predictions_completed.png)

<img src="manga-banner-5e.png" alt="BYTE Manga AI banner" width="20%">




The inference notebook processed all 15 test sequences, with three pages
per sequence. The output JSONL structure was checked before downloading
the predictions file.

![Verified test predictions](screenshots/predictions-verified.png)
<br>
<hr>
<br>

<img src="manga-footer.png" alt="BYTE Manga AI banner" width="100%">

