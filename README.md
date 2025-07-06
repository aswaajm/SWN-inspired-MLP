# SWN-inspired-MLP
Small world network inspired Multi Layer Perceptron(MLP) model 

Objective:
1. Integrate structured sparsity into a dense Multi-Layer Perceptron (MLP) using the Newman–Watts Small-World Network.
2. Introduce asynchronous learning by combining Ridge Regression and SGD for improved training efficiency.

Approach:
1. Performed pruning of low-magnitude weights after 20 epochs of training to identify weak connections.
2. Introduced new connections to non-adjacent layers based on indices of active neurons, with He-initialized weights to preserve gradient flow.
3. Applied Ridge Regression to learn output layer connections (wider subnetwork) and SGD for hidden layers (deeper subnetwork).
4. Retained original hyperparameter settings while reducing the number of active parameters by 10% for fair benchmarking.

Impact:
1. Achieved 65.18% accuracy on the CIFAR-10 dataset, outperforming the dense baseline MLP model by 1.26%.
2. Demonstrated that hybrid sparse architectures can surpass dense models while maintaining lower parameter overhead.
