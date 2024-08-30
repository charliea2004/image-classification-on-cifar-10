# Image Classification on CIFAR-10
Trying out different models for classification on the CIFAR-10 dataset:
- TinyVGG: Here I built the model and trained it from scratch in PyTorch, achieving an accuracy of roughly 75%
- EfficientNet B1: Used transfer learning and finetuned the model on the data. Achieved an accuracy on the test data of around 82%
- EfficientNet B5: Used transfer learning and finetuned the model on the data. Achieved an accuracy on the test data of almost 84%

_EfficientNet is a series of different sized CNNs ranging from B0-B7, with B7 being the largest. As predicted, the much larger EfficientNet-B5 model performs better than EfficientNet-B1._

Some notes:
- Both the EfficientNet notebooks use the utils.py script, which reduces the useful code for importing data and training.
- In all cases I found the testing error to be consistently lower than the training error. After some investigation, I still haven't determined why. I believe this could be related to lower variance in the test data or perhaps in the EfficientNets due to the dropout regularization. Any suggestions would be much appreciated.

Some links:
- [TinyVGG](https://www.researchgate.net/publication/321046304_Understanding_deep_learning_via_backtracking_and_deconvolution)
- [EfficientNet](https://arxiv.org/abs/1905.11946v5)
