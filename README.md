# TensorFlow-Keras-Multi-class-Classifier
The pretrained model 'ResNet50' is retrained to perform multi-class classification of images (apples, bananas and oranges).

## Details
* The model is stored in Hugging Face, use the following link to download it:

https://huggingface.co/AntonioArteaga7/Fruits-Classifier/resolve/main/fruits_classifier.h5

* In folder "notebooks" are the Jupyter Notebooks used to train the model and the Jupyter Notebook "make_multiclass_predictions.ipynb" used to make predictions with the model. This model should be downloaded and saved in folder 'models' as 'fruits_classifier.h5'.
* In folder "test" are some images used to test the model, other images can be also used following the folder structure.

## 🚀 How to use the model locally to make predictions
1. Clone this repository:
```
git clone https://github.com/arteaga7/TensorFlow-Keras-Multi-class-Classifier.git
```
2. Set virtual environment and install dependencies:
```
python3 -m venv env && source env/bin/activate && pip3 install -r requirements.txt
```
3. Create folder "models" and copy the downloaded model into it with the filename 'fruits_classifier.h5'.
4. Run "notebooks/make_multiclass_predictions.ipynb".

## 🎯 Results
After running "make_multiclass_predictions.ipynb", the following results were obtained.

<img width="1065" height="781" alt="image" src="https://github.com/user-attachments/assets/fc35dc9d-bb49-449c-8660-4a0c9a2d56be" />

The metric objective is F1_score and a general accuracy for all classes. There are two types of F1_score, macro and weighted, weighted considers the classes unbalance and the other does not. In this case, classes are balanced.

F1 macro (simple): 0.886, F1 weighted: 0.886 and general Accuracy: 0.889.

## ♟️ Conclusion
The general accuracy is 88.9%. Analyzing the f1_score for each class, it is obtained:
f1_score_apple = 0.8, f1_score_banana = 1 and f1_score_orange = 0.857. The performance of the model is acceptable. In order to improve the model performance, not only the batch size should be increase, but also the dataset quality.
