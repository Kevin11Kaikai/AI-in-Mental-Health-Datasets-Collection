# 🧠 AI in Mental Health: Datasets Collection

This README provides a curated list of publicly available datasets for mental health research using NLP and machine learning. Each dataset is associated with a download link and typically supports tasks like stress detection, suicide risk classification, emotion recognition, causal analysis, etc.

---

## 📂 Dataset List

### 1. [Dreaddit](http://www.cs.columbia.edu/~eturcan/data/dreaddit.zip)
- Task: Stress detection from Reddit posts
- Modality: Text (Reddit)
- SOTA: Logistic Regression with LIWC features ~0.83 F1 (Turcan & McKeown, 2019)

### 2. [SMHD (Self-reported Mental Health Diagnoses)](https://ir.cs.georgetown.edu/resources/)
- Task: Detection of multiple mental illnesses from Reddit
- Modality: Text
- SOTA: BERT-based classifier F1 ~0.85 on depression classification

### 3. [GoEmotions (Google Research)](https://github.com/google-research/google-research/tree/master/goemotions)
- Task: Fine-grained emotion classification (27 emotions + neutral)
- Modality: Text (Reddit comments)
- SOTA: BERT achieves 0.46 macro F1 score (Demszky et al., 2020)

### 4. [MBTI Personality Dataset (Kaggle)](https://www.kaggle.com/datasets/datasnaek/mbti-type?utm_source=chatgpt.com)
- Task: Personality classification based on MBTI types
- Modality: Text (forum data)
- SOTA: LSTM model with ~0.62 accuracy

### 5. [CAMS (Causal Analysis of Mental Health in Social Media)](https://github.com/drmuskangarg/CAMS/tree/main/CAMS/data)
- Task: Causal categorization of mental health issues from Reddit posts
- Modality: Text
- SOTA: RoBERTa w/ CRF ~0.82 F1 on causal explanation span extraction

### 6. [PsySUICIDE (HuggingFace)](https://huggingface.co/datasets/qiuhuachuan/PsySUICIDE)
- Task: Suicide risk classification
- Modality: Text (Chinese + English)
- SOTA: RoBERTa classifier achieves 0.92 F1 on Chinese subset

### 7. [MentalLLaMA Complete Dataset (Reddit + IRF + MultiWD + SAD + Dreaddit)](https://github.com/SteveKGYang/MentalLLaMA/tree/main/train_data/complete_data)
- Task: Multiple mental health NLP tasks
- Modality: Text
- SOTA: LLaMA finetuned with reward alignment (no benchmarks reported yet)

### 8. [RSD_15K](https://github.com/Suicide-DataSet/RSD_15K)
- Task: Suicide detection from Reddit
- Modality: Text
- SOTA: DistilBERT ~0.86 F1 (Suicide-DataSet, 2023)

### 9. [XAI_Suicide Dataset](https://github.com/arekavandi/XAI_Suicide/blob/main/dataset.csv)
- Task: Suicide classification with explainability
- Modality: Text (Reddit)
- SOTA: XGBoost with SHAP explanations ~0.84 F1

### 10. [IRF (Interpersonal Risk Factors in Reddit Posts)](https://github.com/drmuskangarg/Irf)
- Task: Annotated dataset for interpersonal risk factor detection
- Modality: Text
- SOTA: RoBERTa + multi-label classification ~0.76 F1 (Garg et al., 2022)

### 11. [HEAL Dataset](https://github.com/anuradha1992/HEAL/tree/master/data)
- Task: Mental health symptom and support classification
- Modality: Text (Reddit + Twitter)
- SOTA: Logistic Regression with n-grams ~0.70 F1

### 12. [SMILE Dataset](https://github.com/qiuhuachuan/smile/tree/main/data)
- Task: Emotion and suicide-related label classification
- Modality: Text (social media)
- SOTA: BERT-Chinese achieves 0.89 accuracy

### 13. [Suicide and Depression Detection (Kaggle)](https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch)
- Task: Detecting suicidal thoughts and depression from Reddit posts
- Modality: Text (Reddit)
- SOTA: LSTM + Glove achieves ~0.82 F1

### 14. [Suicidal Tweet Detection Dataset (Kaggle)](https://www.kaggle.com/datasets/aunanya875/suicidal-tweet-detection-dataset)
- Task: Classify suicidal vs. non-suicidal tweets
- Modality: Text (Twitter)
- SOTA: BERT-base F1 ~0.89

### 15. [DAIC-WOZ Database (USC ICT)](https://dcapswoz.ict.usc.edu/)
- Task: Multimodal analysis of depression and mental health status
- Modality: Text (transcripts), Audio (participant speech), Visual (facial features)
- SOTA: Multimodal transformer model ~0.78 F1, RMSE ~4.2 on depression severity

---

## 📌 Notes
- Please verify each dataset's license before use.
- For datasets requiring special access (e.g., via signed agreement), follow the respective repository instructions.

Feel free to contribute by submitting a pull request with new datasets!

---

## 📉 Limitations and Research Gaps in Mental Health Datasets

Despite the growing availability of datasets in the field of AI for mental health, several critical **limitations and pain points** remain:

### 🔍 Data Quality & Representativeness

- **Over-reliance on social media**: Most current datasets are derived from Reddit or Twitter, which only offer a partial and often biased view of mental health discourse. These sources lack clinical depth and may **oversimplify complex psychiatric symptoms**.

- **Lack of clinical alignment**: Labels such as “depression” or “suicide risk” are often **assigned without expert validation**, and their definitions vary significantly between datasets. Some labels reflect transient emotional states rather than **clinically diagnosed conditions**.

- **Scarcity of real clinical data**: High-quality, **clinically grounded datasets** suitable for AI model training and validation are **extremely limited**, making it difficult to deploy robust, safe, and reliable AI tools in real-world settings. Even when such datasets exist, **ethical concerns and privacy restrictions** often prevent public access, limiting reproducibility and broader model validation.

- **Lack of standard benchmarks**: Unlike fields like image recognition (ImageNet) or NLP (GLUE), the mental health domain lacks a widely accepted benchmark dataset and evaluation protocol. This hinders fair performance comparisons and slows systematic progress. 


---

## 🤝 AI–Doctor Collaboration Directions

AI systems designed for **collaborative mental health care** are emerging in two key areas:

### 1. 🛑 Early Stage Risk Detection  
AI tools help triage high-risk individuals by **automatically flagging suicidal ideation or distress** in real time from user-generated content. These systems are designed to **assist clinicians**, reducing response time and enabling timely intervention.

### 2. 💬 Early Stage Self-Support and Education  
Conversational agents (e.g., chatbots) are deployed to provide **CBT-based coaching, psychoeducation**, or **low-risk symptom check-ins**, supporting individuals with **mild-to-moderate** symptoms before professional care is needed.

---

## 🧠 Why Interpretability Matters

As AI systems increasingly **interact with vulnerable individuals**, their outputs must be **transparent and trustworthy**:

- For **risk detection**, clinicians need to understand *why* a post or message is flagged as dangerous.
- For **self-support tools**, users deserve clarity on how recommendations (e.g., “try journaling”) are generated.

Therefore, recent research has shifted toward developing models with **built-in explainability**, such as highlighting linguistic cues, extracting causal factors, or generating natural-language rationales.
