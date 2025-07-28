# VITS2: Improving Quality and Efficiency of Single-Stage Text-to-Speech with Adversarial Learning and Architecture Design

...

---

## 🗣️ Armenian TTS Extension (Common Voice 17)

This repository is extended to support Armenian Text-to-Speech (TTS) using the [Common Voice 17](https://commonvoice.mozilla.org/en/datasets) dataset. Before reading this please first read main README.md

- **EDA and Data Preparation:**  
  - See [`EDA`](https://colab.research.google.com/drive/1KM4w5ebHVaWaCY3dsCzZSseMUNz7--Mg?usp=sharing) for exploratory data analysis and speaker selection.
  - See `data_preparation.ipynb` for data cleaning, filtering, and filelist generation.
  This will generate three txt files which are inputs for prepprocess.py
- **Dataset:**  
  - I use the Armenian subset of Common Voice 17, downloaded directly from the [official site](https://commonvoice.mozilla.org/en/datasets).
  - Only high-quality speakers and recordings are included, following a careful EDA process (see notebooks for details).
- **Configuration:**  
  - The configuration for Armenian TTS training is provided in [`configs/common_voice_phonemes.json`](configs/common_voice_phonemes.json).
- **How to Use:**  
  - Follow the original instructions below for environment setup and training.
  - When training on Armenian, use the provided config:
    ```sh
    python train_ms.py -c configs/common_voice_phonemes.json -m armenian_commonvoice
    ```
  - Preprocessing and filelists are generated as described in `data_preparation.ipynb`.

  

---

# Pretrained checkpoints

---

## 🔊 How to Test Armenian TTS Model

After training, you can test (synthesize) Armenian speech using your trained model and the provided config. For example, to generate audio from text:

```sh
python inference.ipynb
```

- Replace `/path/to/your_trained_model.pth` with the path to your trained checkpoint.
Or download mine from here

---





I also did changes in symbols.py and cleaners.py
...