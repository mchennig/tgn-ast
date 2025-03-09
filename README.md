# Leveraging Temporal Graphs for Enhancing Transformer-based Predictive Process Monitoring 

This repository contains the implementation of the TGN-AST hybrid model for predictive process monitoring as described in our paper.

<details>
  <summary>Abstract</summary>
   Predictive process monitoring (PPM) utilizes event logs
  to forecast process outcomes and behaviors. While existing approaches effectively model simple control-flow patterns, they often overlook organizational, and resource information embedded in the event log. Therefore, we develop TGN-AST, a novel hybrid model that leverages this context information to improve prediction, using a design science approach. TGN-AST combines the benefits of temporal graph neural networks and transformer-based sequence modeling to predict processes with resource and organization structures. It ex-tracts organizational relations from event logs as continuous-time dynamic   graphs, learns temporal node embeddings that capture the evolu-tion of relationships, and incorporates these in a  multi-task transformer model. The evaluation of TGN-AST across multiple real-world IT Service Management event logs reveals statistically significant and incremental per-formance improvements, particularly in next activity predictions. The find-ings highlight that integrating a temporal graph network with a transformer enhances predictive performance, bridging the gap between sequential and graph-based process analysis.  Furthermore, our research provides empirical evidence underscoring the utility of temporal context modeling in improving the accuracy and reliability of predictions.
</details>

## Overview

TGN-AST is a novel hybrid approach that combines Temporal Graph Networks (TGN) with Attribute Selection Transformers (AST) to enhance the performance of predictive process monitoring tasks. Our model captures both the temporal graph structure of business processes and the sequential patterns in process execution data.

## Repository Contents

### Notebooks

1. **01_Preprocessing_&_Analysis.ipynb** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1neLmj3AsRGyjel_vnja_435TiLQoztoE)
   - Data preprocessing pipeline
   - Temporal graph generation from process logs
   - Pretraining of the Temporal Graph Network
   - Generation of TensorFlow datasets for model training

2. **02_Model_Development.ipynb** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1neLmj3AsRGyjel_vnja_435TiLQoztoE)
   - Implementation of the TGN-AST hybrid architecture
   - Model training procedures
   - Prediction generation
   - Training monitoring functions

3. **03_Model_Comparison.ipynb** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/19tUGukhW6QRcHhBQtLXs2Lqgim1b5SZS)
   - Comprehensive model evaluation
   - Statistical comparison with baseline models
   - Performance visualization and analysis

#### Requirements Files

For each notebook, we provide a dedicated requirements file to ensure reproducibility:

- `01_requirements.txt` - Dependencies for preprocessing and TGN pretraining
- `02_requirements.txt` - Dependencies for model development and training
- `03_requirements.txt` - Dependencies for evaluation and comparison

### Data Sets

The `datasets/` directory contains the final data sets in Keras / TensorFlow for further use in the model training. 
The archives contain the train and test splits along with all data necessary and can be used after unzipping.

### Results

The `results/` directory contains the predictions generated by our trained models, organized by:
- Prediction task (next activity prediction, remaining time prediction, next timestamp prediction)
- Dataset used for evaluation as described in the paper

## Getting Started

1. Clone this repository:
   ```
   git clone https://github.com/mchennig/TGN-AST.git
   cd TGN-AST-Predictive-Process-Monitoring
   ```

2. Open the notebooks in Google Colab using the badges above, or run them locally after installing the required dependencies.

3. To install dependencies for a specific notebook locally:
   ```
   pip install -r 0X_requirements.txt
   ```

Please note that adjustments of the local variables might be necessary to fit the intended folder structure.
