## Project Description

This project is a bioassay task for anticancer activity prediction, where each chemical compound is represented as a graph, with atoms representing nodes and bonds as edges.
A chemical compound is positive against non-small cell lung cancer, or negative otherwise.

**The experimental protocol used and how was it carried out?**
* 1- Read data file
* 2- Divide content of file based in graphs
* 3- Convert graph data from strings to tensors
* 4- Divide graphs into training and validation
* 5- Will perform oversampling for the training set
* 6- Prepare graph batches for training
* 7 - Models training and evaluation

>During training we will try:
* Different message passing mechanisms
* Different hyperparameter settings for GNN layers
* Will check effect of dense layer configuration on final result of graph classification
* Will check effect of changing batch_size/embedded vector length/ messages length
* We will first start by a baseline model with the default parameters then will try different message passing mechanisms. The best performing technique will be focused more on it in terms of above checks.

**Search space and the criteria to determine good/bad hyper-parameters:**

* The search space covers from the GCN layer hyperparameters to dense layer design to batch_size and embedding vector dimension and messages vector representation length
* we assess hyperparameters and chose them based on performance on validation data

**Problem Definition. What is the input and what is the output:**

* This is a graph-level binary classification task
* each graph is to be predicted to be either 0 or 1 
* each graph represents chemical compound each chemical compound is represented as a graph
* a chemical compound (graph) is positive against non-small cell lung cancer, or negative otherwise
* input is: chemical compound sdf data which will be converted to and represented as graph
* output is: predicting whether the chemical compound (graph) has anticancer activity

**Machine learning task/function required:**
* Binary classification

**What could be the challenges?**
* understanding the SDF file and extracting the information from it
* the class inbalance issue and how to deal with it and its effect on the results
* choosing the suitable message passing mechanism
* what if the data happens to be in need for cleaning how we will deal with it

**The impact**

* The impact of this model is that researches that work in the anticancer medicine research can suggest possible compounds combinations from their domain knowledge that they wanna see if effective or not and instead of phyically manufacturing the compund and test it we can give the model the compound graph data. Graphs that are predicted to be more probable to be anticancer can be focused on and further studied by the researchers and dont waste time or money on compunds that are predicted to be not beneficial. 
* So this model can save money and time that otherwise could be spent on unuseful compounds
* We let researchers focus more on the promising compunds combinations

**What is an ideal solution?**
* The ideal solution was found to be GGNN message passing layer with one single dense layer of 1 unit is used, using batch size of 32 graphs/batch and number GCN layers of 3 with setting the "aggregation_function" hyperparameter to 'mean' instead of maxand using dropout by setting "layer_input_dropout_rate" to 0.3
