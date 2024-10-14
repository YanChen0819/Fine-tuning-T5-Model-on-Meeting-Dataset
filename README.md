# 文本智慧分析 Team 7 Meeting Summarization Project

## Overview
本專案為實作從 hugging face 尋找會議資料集將 T5 Model 針對會議摘要的task做微調訓練，並比較過往研究其他資料集的成果
This project focuses on the **Meeting Summarization task**, an NLP task that condenses a lengthy text document into a shorter version while retaining key information. The project utilizes various meeting datasets and summarization models for evaluation.

## Datasets

| Dataset | Collected Method | Sample Size / Hours |
|---------|------------------|---------------------|
| ICSI (Janin et al., 2003) | PDA | 922 samples / 72 hours |
| AMI (Carletta et al., 2006) | Audio | 54.8K samples / 100 hours |
| MeetingBank (Yebowen Hu et al., 2023) | Video | 6892 samples / 3,579 hours |

## Model and Summarization Performance

| Model | Dataset | ROUGE-1 F1 Score |
|-------|---------|------------------|
| UNS | AMI Meeting Corpus | 37.53 |
| UNS | ICSI Meeting Corpus | 34.11 |
| T5-small | MeetingBank | 58.55 |

The T5-small model used in this project follows a **Text-to-Text framework** and is pretrained on the **C4 dataset**.

## Methodology

- **Dataset**: MeetingBank from Hugging Face, containing meeting records and manually assessed summaries.
- **Preprocessing**: Tokenization of source and target texts using relevant input IDs and attention masks.
- **Modeling**: T5 (Transfer Text-to-Text Transformer) model structure.

## Experiment and Results

Our experiments show that the T5-small model achieves a **ROUGE-1 F1 score of 58.55** on the MeetingBank dataset, significantly outperforming other models.


## Model Comparison

| Model | Dataset | ROUGE-1 F1 Score |
|-------|---------|------------------|
| UNS | AMI Meeting Corpus | 37.53 |
| UNS | ICSI Meeting Corpus | 34.11 |
| T5-small | MeetingBank | 58.55 |

## Conclusion

The T5-small model trained on the MeetingBank dataset demonstrates superior performance in meeting summarization tasks, indicating its effectiveness in processing large datasets.

