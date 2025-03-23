# LuxVeri at GenAI Detection Task 1: Inverse Perplexity Weighted Ensemble  

This repository contains the code and models used for our participation in **Task 1 of the COLING 2025 Workshop on Multilingual Machine-Generated Text (MGT) Detection**.  

## 📌 Competition Overview  

For details on the competition, visit:  
[COLING 2025 Workshop on MGT Detection Task 1](https://github.com/mbzuai-nlp/COLING-2025-Workshop-on-MGT-Detection-Task1)  

## 📝 Task Description  

The competition focuses on binary classification to determine whether a given text is **machine-generated or human-written**. It consists of two subtasks:  

- **Subtask A (English-only MGT detection)**  
- **Subtask B (Multilingual MGT detection)**  

## 🏆 Our Approach & Results  

We developed an **inverse perplexity weighted ensemble** method to improve classification accuracy.  

### **English Track**  
- **Models Used**:  
  - RoBERTa-base  
  - RoBERTa-base + OpenAI detector  
  - BERT-base-cased  
- **Macro F1-score**: **0.7458**  
- **Rank**: **12/35**  

### **Multilingual Track**  
- **Models Used**:  
  - RemBERT  
  - XLM-RoBERTa-base  
  - BERT-base-multilingual-case  
- **Macro F1-score**: **0.7513**  
- **Rank**: **4/25**  

## 📂 Provided Files  

We have submitted Jupyter Notebook (`.ipynb`) files containing our full pipeline, including:  
✅ Data Preprocessing  
✅ Model Training & Fine-tuning  
✅ Inference & Ensemble Predictions  
✅ Evaluation & Submission Formatting  

📌 **Please check the notebooks for complete implementation details.**  

## 🔧 Installation & Usage  

### Environment Setup  

```bash
pip install -r requirements.txt
```
### Running the Notebooks

Open and run the .ipynb files in Jupyter Notebook or Google Colab.


```bash
jupyter notebook
```

### 📊 Evaluation
To validate predictions before submission:

```bash
python format_checker.py --prediction_file_path=predictions.jsonl
python scorer.py --gold_file_path=data/gold_labels.jsonl --prediction_file_path=predictions.jsonl
```

### 📜 Citation
If you use our work, please cite:

```bash
@misc{mobin2025luxverigenaidetectiontask,
      title={LuxVeri at GenAI Detection Task 1: Inverse Perplexity Weighted Ensemble for Robust Detection of AI-Generated Text across English and Multilingual Contexts}, 
      author={Md Kamrujjaman Mobin and Md Saiful Islam},
      year={2025},
      eprint={2501.11914},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2501.11914}, 
}
```