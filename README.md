# adme_property_prediction

## Project aim: 
create a simple pipeline to benchmark a supervised graph neural network, a classical tree model, and a transformer model using ADME data from the TDC

## datasets format and description:
### CYP P450 2C9 Inhibition, Veith et al.
Dataset Description: The CYP P450 genes are involved in the formation and breakdown (metabolism) of various molecules and chemicals within cells. Specifically, the CYP P450 2C9 plays a major role in the oxidation of both xenobiotic and endogenous compounds.

Dataset Statistics: 12,092 drugs.

SMILE Representations: Simplified molecular-input line-entry system, is a specification in the form of a line notation for describing the structure of chemical species using short ASCII strings.

Labels: CYP2C9 inhibition. Binary classification

## Workflow
Train a supervised graph neural network, a tree model and a transformer model with desired dataset
Benchmark the performance of the models and choose an appropriate metric to compare them

### models comparisons
|   | xgboost tree | GNN | Transformer |
| ------------- | ------------- | ------------- | ------------- |
| model description | decision-tree-based ensemble supervised algorithm that uses a gradient boosting framework | deep learning method designed to perform inference on data described by graphs | The pre-trained transformer model named ‘PubChem10M_SMILES_BPE_396_250′ selected from ChemBERTa for fine-tuning |
|  Data preprocessing | transformed into word embeddings using mol2vec where molecules are represented in 300-dimensional vector | transformed into torch_geometric.data.Data objects which represent labeled molecular graphs| tokenizened over SMILES strings using the tokenisation SMILES regex developed by Schwaller et. al.| 
