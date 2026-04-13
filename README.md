# HTF-DTI
HTF-DTI Hypergraph-Based High-Low Order Topological Fusion for Drug-Target Interaction Prediction

HTF-DTI is a deep learning framework designed for drug–target interaction (DTI) prediction. It integrates hypergraph representation learning, graph attention networks (GAT), and a graph-enhanced dual-path interaction module for modeling complex biological relationships.

***

## ✨ Key Features

- 🔗 **Hypergraph Modeling** for high-order biological relationships
- 🧠 **Graph Attention Networks (GAT)** for representation learning
- 🔄 A Graph-Enhanced **Dual-Path interaction module** for interaction modeling
- 📊 Supports multiple benchmark datasets (Luo, Zheng, Yamanishi)

***

## 📂 Project Structure

```
HTF-DTI/
│── main.py                  # Entry point (training & evaluation)
│── model.py                 # Model architecture
│── loaddata_utils.py        # Data loading & preprocessing
│── hypergraph_utils.py      # Hypergraph construction
│── data/
│    ├── Luo/
│    ├── Zheng/
│    └── Yamanishi/
```

***

## ⚙️ Requirements

- Python >= 3.8
- PyTorch >= 1.10
- torch-geometric
- numpy
- scipy
- scikit-learn
- tqdm

Install dependencies:

```bash
pip install torch numpy scipy scikit-learn tqdm
pip install torch-geometric
```

***

## 🚀 Quick Start

Run the model:

```bash
python main.py
```

Default dataset: **Luo**

```markdown
#### data sample `data/Luo` directory
- `drug.txt`: list of drug names  
- `protein.txt`: list of protein names
- `disease.txt`: list of disease names
- `se.txt`: list of side effect names
- `drug_dict_map`: a complete ID mapping between drug names and DrugBank ID
- `protein_dict_map`: a complete ID mapping between protein names and UniProt ID
- `mat_drug_se.txt` 		: Drug-SideEffect association matrix
- `mat_protein_protein.txt` : Protein-Protein interaction matrix
- `mat_protein_drug.txt` 	: Protein-Drug interaction matrix
- `mat_drug_protein.txt`: Drug_Protein interaction matrix
- `mat_drug_drug.txt` 		: Drug-Drug interaction matrix
- `mat_protein_disease.txt` : Protein-Disease association matrix
- `mat_drug_disease.txt` 	: Drug-Disease association matrix
- `Similarity_Matrix_Drugs.txt` 	: Drug similarity scores based on chemical structures of drugs
- `Similarity_Matrix_Proteins.txt` 	: Protein similarity scores based on primary sequences of proteins
```

To switch datasets, edit:

```python
for name in ["Luo", "Zheng", "Es", "GPCRs", "ICs", "NRs"]:
```

***

## 🧪 Training Details

- Optimizer: Adam
- Learning Rate: 0.0001
- Epochs: 100
- Dropout: 0.2
- Weight Decay: 1e-10
- Cross Validation: 5-fold

***

## 📊 Evaluation Metrics

- AUROC
- AUPR
- F1-score
- Accuracy

***

