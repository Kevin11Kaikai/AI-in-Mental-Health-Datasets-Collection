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

### 🔍 Data Quality & Representativeness ⚠️

- **Over-reliance on social media**: Most datasets are derived from Reddit or Twitter, which only offer a biased and incomplete view of mental health. These sources lack clinical depth and may oversimplify psychiatric conditions.  
  *Supported by:* [Choudhury et al., 2025 – *Large Language Models in Mental Health Care: A Scoping Review*](https://www.nature.com/articles/s41746-025-01611-4)

- **Inconsistent label definitions**: Terms like “depression” or “suicide risk” are often loosely defined across datasets and lack validation from mental health experts, leading to variable interpretations of what constitutes clinical risk.  
  *Supported by:* [Choudhury et al., 2025 – *Large Language Models in Mental Health Care: A Scoping Review*](https://www.nature.com/articles/s41746-025-01611-4)

- **Scarcity of high-quality clinical datasets**: Clinically grounded datasets suitable for model development and validation are rare. Even when available, ethical and privacy restrictions often prevent public access, limiting reproducibility and validation.  
  *Supported by:* [Choudhury et al., 2025 – *Large Language Models in Mental Health Care: A Scoping Review*](https://www.nature.com/articles/s41746-025-01611-4)

- **Lack of standard benchmarks**: Unlike ImageNet in vision or GLUE in NLP, mental health doesn’t have widely accepted benchmark datasets or evaluation protocols, making performance comparisons across studies difficult and slowing field-wide progress.  
  *Supported by:* [Choudhury et al., 2025 – *Large Language Models in Mental Health Care: A Scoping Review*](https://www.nature.com/articles/s41746-025-01611-4)



---

## 🤝 AI–Doctor Collaboration Directions

AI systems designed for **collaborative mental health care** are emerging in two key areas:

### 1. 🛑 Early Stage Risk Detection  
AI tools help triage high-risk individuals by **automatically flagging suicidal ideation or distress** in real time from user-generated content. These systems are designed to **assist clinicians**, reducing response time and enabling timely intervention.  
*Supported by:* [Hua et al., 2024 – *Large Language Models in Mental Health Care: A Scoping Review*](https://www.nature.com/articles/s41746-025-01611-4)

### 2. 💬 Early Stage Self‑Support & Education  
Conversational agents (e.g. chatbots) provide **CBT‑based coaching, psychoeducation**, or **low‑risk symptom check‑ins**, supporting individuals with **mild‑to‑moderate** symptoms before professional care is needed.  
*Supported by:* [Hua et al., 2024 – *Large Language Models in Mental Health Care: A Scoping Review*](https://www.nature.com/articles/s41746-025-01611-4)


---

## 🧠 Why Interpretability Matters

As AI systems increasingly **interact with vulnerable individuals**, their outputs must be **transparent and trustworthy**:

- For **risk detection**, clinicians need to understand *why* a post or message is flagged as dangerous—identifying which linguistic cues triggered the alert and whether the reasoning aligns with clinical judgment.  
  *Supported by:* A systematic review emphasizes that interpretability (e.g., XAI methods) significantly influences clinicians’ trust in AI-generated risk assessments, but only when explanations are coherent and clinically meaningful. ([JMIR AI Trust Review, 2024](https://ai.jmir.org/2024/1/e53207), see “explanations enhance clinicians’ trust”) :contentReference[oaicite:1]{index=1}

- For **self-support tools**, users deserve clarity on how recommendations (e.g., “try journaling”) are generated, to build transparency and adherence. Interpretability helps users feel confident that advice is reasoned and safe.  
  *Supported by:* Research in digital health underscores that explainability not only aids clinician oversight but also improves user acceptance and safety perception in sensitive applications like mental health. ([Explainable AI for Mental Health, PMC 2022](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9849399/)) :contentReference[oaicite:2]{index=2}

- Overall, interpretability is essential for establishing **clinical trust, accountability, and safety** in AI‑augmented mental health systems.  
  *Supported by:* Broader AI-in-healthcare reviews confirm that transparent models enable effective oversight and continuous improvement—key for deploying decision-support tools in clinical settings. ([WHO‑aligned XAI framework for e‑Health interventions, 2023](https://arxiv.org/pdf/2311.11055)) :contentReference[oaicite:3]{index=3}


Therefore, recent research has shifted toward developing models with **built-in explainability**, such as highlighting linguistic cues, extracting causal factors, or generating natural-language rationales.
