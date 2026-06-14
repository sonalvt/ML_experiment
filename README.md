# ML_experiment
Project Overview
The goal was to understand how different training parameters affect the model’s performance. I made a dataset of 60 images of spoons and forks under different lighting conditions, disturbances in the background and viewing angles.

Experiments and Observations:
1. Baseline Model:
The model trained normally and both the training loss and validation loss decreased over time. Accuracy improved steadily, which showed that the model was learning useful features from the images.

2. Learning Rate:
I experimented with different learning rates to see how they affect training.
Very Small Learning Rate (0.0001)
The model learned very slowly. The loss decreased gradually, but it took much longer for the model to improve.
Normal Learning Rate (0.001)
This gave the most stable results. The model learned at a reasonable speed and training remained stable.
Very Large Learning Rate (10.0)
This was my failed experiment.
The training became unstable and the loss fluctuated heavily. Instead of improving, the model struggled to converge. This helped me understand that a learning rate can be too large, causing the optimizer to overshoot good solutions.

3. Regularization Experiment:
I compared training with and without dropout.
Without dropout, the model achieved very high training accuracy. At first I thought this meant the model was better, but the validation performance did not improve by the same amount.
This helped me understand overfitting. The model was starting to memorize the training images instead of learning general features.
Adding dropout made training slightly harder, but it helped the model generalize better.

4. Batch Size Experiment
I compared different batch sizes,with a smaller batch size, the training curves looked noisier because the model updated its weights more frequently, but with a larger batch size, the training curves appeared smoother.
This showed me that batch size affects how the model learns and how stable the training process looks.

5. Optimizer Comparison
I compared SGD and Adam optimizers.Adam generally converged faster and reached good performance more quickly. SGD also worked, but it required more time and training before reaching similar performance. This helped me understand that optimizer choice can significantly affect training speed.

Insights and Takeaways

The biggest takeaway from this project is that training neural networks is not just about building a model. A lot of the performance comes from choosing the right training settings.

Some things I learned:

High accuracy on training data does not always mean the model is good.
Overfitting can happen very easily on small datasets.
Learning rate has a huge impact on training behavior.
Dropout helps improve generalization.
Different optimizers can lead to very different results.
Looking at loss curves can tell a lot about how a model is learning.

