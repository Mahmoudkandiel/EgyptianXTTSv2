# EgyptianXTTSv2

FineTuned XTTS v2 model to generate Egyptian speech using a custom-made dataset. This model is trained with a pipeline that processes YouTube data into a usable dataset.


---
![XTTS V2 architecture](https://github.com/user-attachments/assets/ed684820-38e6-41d9-9925-e9a286baaf41)
## Table of Contents

1. [Model Overview](#model-overview)
2. [Dataset Pipeline](#dataset-pipeline)
3. [Training Details](#training-details)
4. [Outputs](#outputs)
5. [How to Use](#how-to-use)
6. [Future Work](#future-work)

---

## Model Overview

This model was fine-tuned using approximately **15 hours** of Egyptian speech sourced from YouTube. The primary source of the data is the YouTube channel **(فيلم فى الخمسينة)**, which provides high-quality Egyptian Arabic speech recordings.

---

## Dataset Pipeline
You can find the dataset pipeline implementation [Youtube_Dataset.ipynb](https://github.com/Mahmoudkandiel/EgyptianXTTSv2/blob/main/Youtube_Dataset.ipynb).

**The link of the URL must contain videos with arabic auto-genrated subtitles only**

A custom dataset pipeline was designed to process and prepare the audio data. The pipeline includes the following steps:

1. **Data Collection:** Extract audio and auto-genrated subtitles content from YouTube videos.
2. **Annotation:** Segment and label the audio to match the requirements for speech synthesis.
3. **Dataset format:** format dataset in LJspeech format required for training the XTTS v2 model.

This pipeline ensures that the dataset is clean , normalized, well-structured, and ready for fine-tuning.

---

## Training Details

- **Base Model:** XTTS v2
- **Fine-Tuning Data:** 15 hours of Egyptian Arabic speech
- **Source:** YouTube (primarily from فيلم فى الخمسينة)
- **Training steps:** 18,000

---

## Outputs

The fine-tuned model generates high-quality Egyptian Arabic speech that closely resembles the source data. Below are some audio samples:

- [Sample 1](https://github.com/user-attachments/assets/82a110cc-7718-4f69-a753-be53de74ae7c)
- [Sample 2](https://github.com/user-attachments/assets/f77a66d0-cb02-4644-9e30-33b79ac92879)
- [Sample 3](https://github.com/user-attachments/assets/9d0326ec-0f85-4367-b2c5-1097292c3baf)

---

## How to Use

1. Run the EG_XTTSv2.pyinb file in colab 
2. Download the required files  
3. go to model infernce at the end to generate audio
---

## Future Work

- Expanding the dataset to include more diverse speakers and topics.
- Improving the pipeline for faster dataset creation.
- Fine-tuning with additional speech synthesis models for comparison.

---

For any questions or contributions, feel free to open an issue or submit a pull request!

