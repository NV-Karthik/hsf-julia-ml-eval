# hsf-julia-ml-eval
Evaluation Excersice Submission for the Machine Learning in Julia for Calorimeter Showers HSF GSoC Project

## The contents in the readme are elaborated in the jupyter notebook, explaining necessary portions of the code at appropriate places

1. From a preliminary look into the dataset, it can be seen that the dataset is <b>normalized</b> but is also <b>skewed</b>.
2. It is asked to perform a binary classification of point set into the labels "signal" or "background".
3. Feature arrays are independent (point co-ordinates) and are less in number, so a simple neural network with traditional sigmoid activation is expected to produce accurate results without overfitting
4. Thus, a network with 1 hidden layer containing 10 neurons with <b>sigmoid</b> activation is chosen as a first step.
5. <b>Binary Cross Entropy</b> loss function, and <b>Adam Optimizer</b>, known to be the simplest and the best-performing choices for binary classification task, are chosen in this model.
6. Learning rate of 0.01 and default momentum parameters ie.,(0.9, 0.999), are chosen. Again, to start from the simplest and lightweight model
7. The training loop operated for 1000 epochs, which was decided on iterative basis with the help of the <b>loss vs epochs plot</b>, included in the repo.
8. Satisfactory results (<b>>95%</b>) of <b>accuracy, F1, recall, precision, and balanced accuracy</b> are obtained both for the whole dataset and also a "<b>test set</b>" split before the training phase.
9. Thus to avoid overfitting, and use unnecessary compute resource, I deem this model to be simple and suitable for the prescribed task of binary classification 
