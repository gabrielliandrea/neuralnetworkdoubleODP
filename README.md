# A Neural Network Boosted Double Over-Dispersed Poisson Claims Reserving Model
The purpose of this project is to present a claims reserving technique that takes into account both claim counts and claim amounts. The main reason for considering such a joint model is that adding claim counts information should improve the prediction of future claim amounts. We start with defining two separate ccODP models for the claim counts and the claim amounts. Then, we jointly embed the two separate ccODP models into a neural network architecture. This neural network will have a two-dimensional output vector, as we need to simultaneously model future claim counts and future claim amounts. As starting point of the neural network calibration we use exactly the two separate ccODP models. Training of the neural network then allows us for joint modeling and mutual learning of the claim counts and the claim amounts beyond the two individual ccODP models.

The relevant R code is provided in the zip file [ANeuralNetworkBoostedDoubleOverDispersedPoissonModelGithub.zip](https://github.com/gabrielliandrea/neuralnetworkdoubleODP/blob/master/ANeuralNetworkBoostedDoubleOverDispersedPoissonModelGithub.zip). On the one hand, in the file `SingleNNDODPModel.r` we consider a separate neural network embedding for every line of business. On the other hand, in the file `MultipleNNDODPModel.r` we model multiple lines of business simultaneously. Such a model allows us to learn additional information across the different lines of business. For the theoretical details we refer to the corresponding [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3365517).
