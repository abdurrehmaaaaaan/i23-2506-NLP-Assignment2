# i23-2506-NLP-Assignment2

CS-4063 Natural Language Processing — Assignment 2: Neural NLP Pipeline  
FAST NUCES

---

## Requirements

Python 3.9 or higher is required.

Install all dependencies with:

```bash
pip install torch numpy scikit-learn matplotlib
```

---

## Input Files

Place the following files in the root directory of the project before running anything:

| File | Purpose |
|---|---|
| `cleaned.txt` | Primary training corpus (preprocessed BBC Urdu) |
| `raw.txt` | Unprocessed corpus used in ablation C2 |
| `Metadata.json` | Article metadata with titles, used for topic labels |

These files are from Assignment 1 and are not included in this repository.

---
The `embeddings/`, `models/`, and `data/` directories are created automatically when the notebook is run.

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/i23-XXXX-NLP-Assignment2.git
cd i23-XXXX-NLP-Assignment2
```

2. Place `cleaned.txt`, `raw.txt`, and `Metadata.json` in the root directory.

3. Install dependencies:

```bash
pip install torch numpy scikit-learn matplotlib
```

4. Open the notebook:

```bash
jupyter notebook i23-XXXX_Assignment2_DS-X.ipynb
```

5. Run all cells in order from top to bottom using **Kernel → Restart & Run All**.

Do not skip cells or run them out of order. Each part depends on variables defined in previous cells.

---

## Parts

| Part | Description |
|---|---|
| Part 1 | Word Embeddings — TF-IDF, PPMI, Skip-gram Word2Vec |
| Part 2 | Sequence Labeling — BiLSTM POS Tagger and NER with CRF |
| Part 3 | Transformer Encoder for Topic Classification |

---

## Notes

- Training is done on CPU by default. If a CUDA GPU is available it will be used automatically.
- Part 1 Skip-gram training takes approximately 15–20 minutes on CPU for 5 epochs over the full corpus.
- Part 2 BiLSTM training takes approximately 5 minutes per model on CPU.
- Part 3 Transformer training takes approximately 10 minutes on CPU for 20 epochs.
- All output files (embeddings, models, CoNLL data) are saved automatically during the run.
