## Run all models
1. Download the [`notebook`](#https://github.com/Ahn-Ssu/CS492I_2022F/blob/main/CS492I_teamProject_GCN4chem.ipynb). You can upload to Google Colab or run on your own computer.
2. Add files in [‘data’](#https://github.com/Ahn-Ssu/CS492I_2022F/tree/main/data) to your working directory. 
3. Run cells in 1 to 4. Skip 5.
4. To see sample plot, run cells in 6


## Run the best model
1. Download the [`notebook`](#https://github.com/Ahn-Ssu/CS492I_2022F/blob/main/CS492I_teamProject_GCN4chem.ipynb). You can upload to Google Colab or run on your own computer.
2. Add files in [‘data’](#https://github.com/Ahn-Ssu/CS492I_2022F/tree/main/data) to your working directory. 
3. Run cells in 1 to 3, and data loading cells in 4-1 and 4-2
4. Run cells in 5

Below is a brief description of the notebook. 

## 1. Data load 
### 1-1. Generating feature matrix via the paper way
- load_ZINCdataset1 and load_CEPdataset1 returns data including one-hot encoded matrix of atomic features
### 1-2. Variation of the features
- load_ZINCdataset2 and load_CEPdataset2 returns data including atomic feature and molecular feature encoded matrix
 ## 2. Model Implementation
### 2-1. GatedSkipConnection (GATE) & SkipConnection
- implementation of skip connection and gated skip connection
### 2-2 Graph Convolutional Networks
implementations of 
Attention and gate-augmented graph convoutional networks
- Graph Convolutional Networks (GCN) with skip connection
- Graph Convolutional Networks (GCN) with gated skip connection
- Graph Attention Networks (GAT) with skip connection
- Graph Attention Networks (GAT) with gated skip connection 

Graph Isomorphic Networks
- Graph Isomorphic Networks (GIN) 
- Graph Convolution Netowkrs (GCN)
- Graph SAmple and aggreGatE (SAGE); mean aggregator version

**3 Modified SAGE layer**
## 3. Training
### 3-1. Train, test and runner functions
## 4. Experiments
### 4.1 Experiment 1; one-hot feature training
- run torch models GCNwithSkip, GCNwithGate, GATwithSkip, GATwithGate, and torch_geometric models GIN, GCN, SAGE, modified_SAGE with data loaded by 1-1 functions
### 4.2 Experiment 2; atomic feature training 
- run the same models by loading data (1-2) with args.mol_dim = 0
### 4.3. Experiment 3; training with atomic and molecular features
- run the same models by loading data (1-2) with args.mol_dim = 19
## 5. Best model, configuration, and data representation methods
- hyperparameter settings for best performance in LogP, TPSA, SAS, CEP
- the pretrained model load function
## 6. Plotting result
- Reproducing result
- Compare three feature encodings
