# machine learning experiments across several datasets
This repo compares machine learning algorithms across 4 datasets and 2 reinforcement learning environments. The first 3 datasets are used to compare Decision Tree (DT), Support Vector Machine (SVM) and Neural Network (NN) based algorithms across different types of tasks and data: regression, multi- class classification and a classification task using complex image data. The next dataset is a relational learning task used to compare rule-learning time for different Inductive Logic Programming (ILP) systems on the UW-CSE dataset. Finally, two types of reinforcement learning algorithm Q-learning and Sarsa are compared across two environments from the Gymnasium toolbox. On the regression task SVM performed best, on both classification tasks DT performed best. On ILP, PyGol performed better than Aleph with regards to both learning time and accuracy. Q-learning outperformed Sarsa in both environments.
<br /><br />
**All details about the datasets, experiments, models used, and results are documented in the Report uploaded here.**

## Datasets
### Dataset 1 – Boston Housing Prices
Dataset 1 is a regression task with non-linear dependencies between features. The dataset contains information on the various factors that influence house prices in Boston, Massachusetts, USA. There are 13 attributes being used to predict the target variable: MEDV (house price).

### Dataset 2 – Room Occupancy
Dataset 2 is a multiclass classification task for predicting the number of occupants in a room, ranging from 0 to 3. There are 16 attributes to the data and 10129 instances, the attributes correspond to 4 sensors for sound, light and temperature, a CO2 sensor measures both ppm as well as slope from a sliding window and 2 motion detectors. The data is all numerical, with no null values so minimal data cleaning is required.

### Dataset 3 – Healthy/Diseased Leaf Images
Dataset 3 is an image dataset for a binary classification task for classifying images of leaves as healthy or diseased. This can be downloaded from [here](https://drive.google.com/file/d/1ErfQkvVTgwyFJB-ekjyFvAofu6PmsrTQ/view?usp=sharing).

### Dataset 4 – ILP
The dataset consists of a set of Prolog clauses that encode relationships between entities within the UW-CSE (University of Washington Computer Science and Engineering) domain. These clauses represent aspects such as student-advisor relationships, courses, publications, and other relevant information related to the academic domain.

### Reinforcement Learning Environments
To compare reinforcement learning algorithms two environments were used from the Gymnasium Toy Text project. The first environment used was Taxi, this problem requires the algorithm to pick up passengers and drop them at the correct location.<br />
The second environment explored was Cliff Walking from the same environment library as before. In this case, the Cliff Walking problem requires the algorithm to avoid falling off a cliff when crossing a gridworld from start to goal.

## Experiments
### Null Hypothesis 1
Comparing the relative performance, effectiveness, and interpretability of the SVR, DT, and MLP models for a regression task of predicting housing prices in the Boston area. SVR and MLP methods are expected to have better generalization given the high dimensionality of the dataset.
### Null Hypothesis 2
This experiment looked to verify the null hypothesis that the DT based algorithm, random forest, would outperform SVM and MLP on a less complex dataset for a multiclass classification task where the data is imbalanced.
### Null Hypothesis 3
Comparing the performance of DTs, SVC, and CNNs for a binary classification task on an image dataset. Null hypothesis being “CNNs are more accurate and efficient at classifying images than DT and SVC due to their ability to capture complex image information”.
### Null Hypothesis 4
Comparing rule-learning time for different Inductive Logic Programming systems. The null hypothesis being: "There is no significant difference in the convergence ability of Aleph and PyGol to generate a single rule that satisfies all the training examples."
### Null Hypothesis 5
Q-learning expected to converge on a better optimal policy but Sarsa to perform better in training as Q-learning optimises the Q-values using an “off-policy” method whilst Sarsa uses “on-policy”.

## Requirements for each notebook
**D1_BOSTON_exploration_models.ipynb**: requires housing.csv to be downloaded in the same repository as the notebook<br />
**Dataset2_exploration_and_experimentation.ipynb**: requires Occupancy_Estimation.csv to be downloaded in the same repository as the notebook<br />
**leaf_exploration_final.ipynb**: requires [leaf_dataset_small.zip](https://drive.google.com/file/d/1ErfQkvVTgwyFJB-ekjyFvAofu6PmsrTQ/view?usp=sharing)<br />
**leaf_dataset_model_construction.ipynb**: requires [leaf_dataset_small.zip](https://drive.google.com/file/d/1ErfQkvVTgwyFJB-ekjyFvAofu6PmsrTQ/view?usp=sharing)<br />
**CNNleafdataset_final.ipynb**: requires [leaf_dataset_small.zip](https://drive.google.com/file/d/1ErfQkvVTgwyFJB-ekjyFvAofu6PmsrTQ/view?usp=sharing)<br />
**ILP_Aleph_vs_PyGol.ipynb**: requires ILP_Files.zip to be unzipped in the same repository as the notebook<br />
**Cliff_walking_Reinforcement_learning.ipynb**: dataset imported from gymnasium website, NO requirements<br />
**Reinforcement_learning_Taxi_environment.ipynb**: dataset imported from gymnasium website, NO requirements<br />


## Acknowledgements
University of Surrey project team:
[Steryios Nicolaides](https://www.linkedin.com/in/steryios-nicolaides-7a02511b0/) • [Jamie Prestwich](https://www.linkedin.com/in/james-prestwich/) • [Pauline Schouten](https://www.linkedin.com/in/pauline-schouten-b77208235/) • [Rudra Someshwar](https://www.linkedin.com/in/itsrudra/) 

Project supervisor: [Dr. Alireza Tamaddoni-Nezhad](https://www.surrey.ac.uk/people/alireza-tamaddoni-nezhad)

