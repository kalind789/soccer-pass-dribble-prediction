# soccer-pass-dribble-prediction

The objective of this project was to train a model to classify a clip as a "pass" or dribble." The motivation for this was the need for large labeled datasets in soccer-specific contexts. Developing a pipeline that could be fed a soccer game recording and output a labeled dataset of short clips with labels of pass or dribble could prove useful for training desicion models. These subsequent models would then have the training data they need in order to predict whether a player SHOULD pass or dribble. 

We manually labeled 2k+ clips from soccer games to train our model. We used a pre-trained SlowFast model with a ResNet-50 backbone and fine-tuned the last layers to our use case. We achieved ~70% accuracy. 

- 445_KaKa_Final_Report.pdf contains our final project report. 
- model-dev.ipynb contains the pipeline for fine-tuning the model and evaluating baseline and fine-tuned model accuracy. 
- data-collection.ipynb contains the pipeline for manually labeling the soccer clips.

### Set up
- Make sure you have conda installed: https://docs.anaconda.com/anaconda/install/
- Create a conda environment for this project: conda create --name deep_learning_project python=3.9
- Activate the enviroment: conda activate deep_learning_project
- Install the needed packages ([Pytorch](https://pytorch.org/get-started/locally/) shown): conda install pytorch torchvision -c pytorch
- Download juypter: conda install jupyter
- Open up jupyter: jupyter notebook
