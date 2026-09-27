# AI-Drug-Discovery-and-Repurposing
AI-driven drug repurposing through drug–disease link prediction and drug–drug interaction safety analysis using Graph Neural Networks.

This project explores the use of Artificial Intelligence and Graph Neural Networks for computational drug discovery and drug repurposing.

The system combines biomedical information from multiple sources to learn relationships between drugs, diseases, genes, proteins, and other biomedical entities.

The project focuses on two main tasks:

* Drug-Disease Link Prediction - identifying potential associations between existing drugs and diseases.
* Drug-Drug Interaction Analysis - analyzing drug pairs and classifying their potential interaction severity.

## Project Workflow

* Biomedical Data Collection
* Knowledge Graph Construction
* Molecular Feature Extraction
* Graph Neural Network Training
* Drug-Disease Link Prediction
* Drug-Drug Interaction Analysis
* Model Evaluation
* Repurposing Candidate Analysis

## Drug Repurposing

Drug repurposing aims to identify new therapeutic uses for existing drugs.

This project formulates drug repurposing as a drug-disease link prediction problem on a heterogeneous biomedical knowledge graph.

The graph incorporates:

* Drugs
* Diseases
* Genes
* Proteins
* Drug targets
* Drug-disease associations
* Gene-disease associations
* Other biomedical relationships

The model learns representations from these relationships and predicts potential drug-disease associations.

## Drug-Drug Interaction Analysis

The second component focuses on Drug-Drug Interactions (DDIs).

The system analyzes drug pairs and classifies their potential interaction severity into:

* Safe
* Moderate
* Severe

The classifier uses molecular features and learned drug representations to model relationships between drug pairs.

## Model Architecture

### Graph Neural Network

The drug repurposing component uses a Graph Neural Network to learn representations of drugs and diseases from the biomedical knowledge graph.

The model learns from:

* Graph structure
* Biomedical relationships
* Drug molecular characteristics
* Neighboring entity information
* Drug and disease embeddings
* Graph-based message passing

### Molecular Features

Drug representations incorporate molecular and physicochemical information including:

* Molecular weight
* LogP
* Hydrogen-bond donors
* Hydrogen-bond acceptors
* TPSA
* Rotatable bonds
* Molecular fingerprints
* Other molecular descriptors

Morgan molecular fingerprints are used to capture structural characteristics of drug molecules.

## Dataset

The project integrates information from multiple biomedical resources.

| Source   | Purpose                                    |
| -------- | ------------------------------------------ |
| PrimeKG  | Biomedical knowledge graph                 |
| DrugBank | Drug information, targets and interactions |
| CTD      | Chemical, gene and disease associations    |

The original datasets are not included in this repository where redistribution or licensing restrictions apply.

Users should obtain the required datasets from their respective official sources and comply with their terms of use.

## Results

### Drug-Disease Link Prediction

| Metric              | Result |
| ------------------- | -----: |
| AUROC               | 0.9976 |
| AUPRC               | 0.9959 |
| F1 Score            | 0.9965 |
| Validation Accuracy |  0.998 |
| Test Accuracy       |  0.996 |

### Drug-Drug Interaction Classification

| Metric        | Result |
| ------------- | -----: |
| Test Accuracy | 87.69% |
| Macro F1      | 0.5618 |
| Classes       |      3 |

The difference between accuracy and Macro F1 reflects the challenge of class imbalance across the drug interaction severity categories.

## Technologies Used

### Machine Learning

* Python
* PyTorch
* PyTorch Geometric
* Scikit-learn

### Graph and Data Processing

* NetworkX
* Pandas
* NumPy
* lxml

### Cheminformatics

* RDKit
* Morgan Molecular Fingerprints
* Molecular Descriptors

### Model Evaluation

* AUROC
* AUPRC
* F1 Score
* Accuracy
* Confusion Matrix

### Environment

* Google Colab
* GPU-based training

## Repository Structure

* data/ - Dataset-related files and documentation
* notebooks/ - Main project notebook
* outputs/ - Trained models and evaluation results
* figures/ - Generated visualizations
* requirements.txt - Python dependencies
* .gitignore - Files excluded from Git
* README.md - Project documentation

## Running the Project

### 1. Clone the Repository

Clone the repository and navigate to the project directory.

### 2. Install Dependencies

Install the required Python packages using the requirements.txt file.

### 3. Prepare the Data

Obtain the required datasets from their official sources and place them in the appropriate data directory.

### 4. Run the Notebook

Open the main project notebook using Google Colab or Jupyter Notebook and run the cells sequentially.

The notebook covers:

* Data preparation
* Knowledge graph construction
* Molecular feature generation
* GNN training
* Drug-disease prediction
* Drug-pair feature generation
* DDI classification
* Model evaluation

A GPU-enabled environment such as Google Colab is recommended for model training.

## Applications

This project demonstrates potential applications of Artificial Intelligence in:

* Computational drug discovery
* Drug repurposing
* Drug-disease association prediction
* Drug-drug interaction analysis
* Biomedical knowledge graph analysis
* Molecular representation learning
* AI-assisted pharmaceutical research

## Limitations

* Biomedical datasets may contain incomplete relationships.
* Drug-drug interaction datasets can have significant class imbalance.
* Model performance depends on the quality and coverage of the underlying datasets.
* Computational predictions require biological and experimental validation.
* Predicted relationships should not be interpreted as clinical evidence.

## Future Improvements

* Incorporate additional biomedical knowledge graphs.
* Use molecular Graph Neural Networks for richer drug representations.
* Add protein-drug interaction information.
* Improve minority-class DDI detection.
* Add explainability to GNN predictions.
* Validate predictions using independent datasets.
* Develop an interactive interface for exploring predictions.

## Disclaimer

This project is intended for academic and research purposes.

The predictions generated by the models are computational results and should not be interpreted as medical advice, treatment recommendations, or evidence of clinical efficacy or safety.
