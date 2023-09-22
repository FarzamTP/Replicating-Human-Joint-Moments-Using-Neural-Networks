# Replicating-Human-Joint-Moments-Using-Neural-Networks

The goal of this project is to investigate how well a neural network can imitate human gait in a
prosthesis. For this, it is important to not only look at “normal” gait but also to compare how the
robot/controller and human react to perturbations, deviations from normal.
In the dataset, the upwards and forwards direction are positive, as well as forward lean of the trunk,
hip flexion, knee flexion and ankle plantarflexion for both the joint angles and joint moments.

You will use a dataset of a recording of perturbed gait to not only investigate how well normal
walking is replicated, but also perturbed movements. This dataset contains the joint angles of all
joints and the joint moments of the joint(s) for which you are creating the controller. The joint angles
are the inputs to the controller, while the joint moments are the outputs. The calculated moments
from the controller are then compared to the moments that are in the dataset.
The next task is to set up the neural networks. The neural network should predict the joint moment
for each time point. You can use a convolutional neural network that only looks at the information at
the current time point, but also a recurrent neural network using a short time history. The goal is to
compare different input combinations, such as only using the joint angle of the joint for which you
are creating the controller, all joint angles, or both these options combined with the ground reaction
force. The idea is that, if only one joint angle is sufficient, then less sensors will be required in a
prosthesis or exoskeleton, which makes them cheaper and less prone to failure.
Next, the goal is to train the neural networks. When dividing into training and testing data, you need
to take care of the temporal dependence of the data (I can give you some more hints, but would like
you to think about how to do this yourself). Finally, you will compare the test data predictions to the
ground truth. Make sure that you not only look at the loss and error numbers, but also investigate
the graphs to interpret your results.

[Full Credit to [Prof. Dr. Koelewijn](https://www.mad.tf.fau.de/person/anne-koelewijn/)]
