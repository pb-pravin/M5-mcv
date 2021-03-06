## RETHINKING THE INCEPTION ARCHITECTURE FOR COMPUTER VISION
This model has the goal of reducing the number of parameters needed to achieve a high accuracy. For instances this model have 12x reduction with respect to AlexNet, and also has less than VGGNet which have 3x more than AlexNet. The drawback is that the complexity of the net make more difficult to change its architecture and the little information about the various design decision makes GoogLeNet a complex architecture.

The design follow a basic set of principles. Avoid bottlenecks in the early layers, the size usually should decrease in the depth. Higher dimensional representation is easier to process locally; this makes possible to train faster. Spatial aggregation can be done over lower dimensional embedding. Balance the width and depth of the network. Sometimes is difficult to apply these principles.

One of the way to reduce the number of parameters is factorizing convolutions with large filters. It also improves the computationally efficient as it also reduces the number of activation. The best way to factorizing the convolutional layers is to replace this layers for ones smaller. The experiments show that using this method it also gains in performance supposedly because it adds more variation moreover if it is use with batch-normalization. Another factorization could be use asymmetric convolution; a single layer could be split in to single dimension layers. In this case the results shows that there isn�t any improvement in the early layers. However, in medium grid-size they get a good result.

Other method test is to use auxiliary classifiers but the results where that the net doesn�t converge early because the network with branch overtake the accuracy of the network without branch. These auxiliary classifiers could be used as a regularization.

One main improvement is to use efficient grid size reduction using two parallel stride replacing the traditional convolutional layer plus pooling operation.

This paper also includes a propose of regularization via label smoothing. With this the model is less confidence but it makes more adaptable.

In the lower resolution inputs, the net could perform well compare to the other resolution but the model usually take longer to train and to perform more poorly, if the reduction is to aggressive. This kind of networks are good to detected small objects in the scene.
