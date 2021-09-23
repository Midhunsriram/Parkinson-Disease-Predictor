# Parkinson's-Disease-Predictor
Predicting Parkinson's Disease from a dataset of spiral, wave hand-drawn images by Healthy as well as Parkinson's Patients.

### WHAT IS PARKINSON'S DISEASE
- A disorder of the central nervous system that affects movement, often including tremors.
- Parkinson's often starts with a tremor in one hand. Other symptoms are slow movement, stiffness and loss of balance.
Medication can help control the symptoms of Parkinson's.
- One of the symptoms of Parkinson’s is tremors and rigidity in the muscles, making it harder to draw smooth spirals and waves.
### HOW TO PREDICT IT USING ML?
- A 2017 study by Zham et al. found that it was possible to detect Parkinson’s by asking the patient to draw a spiral and then track:
1. Speed of drawing
2. Pen pressure
- Link to a detailed paper --> https://www.frontiersin.org/articles/10.3389/fneur.2017.00435/full
- The researchers found that the drawing speed was slower and the pen pressure lower among Parkinson’s patients — this was especially pronounced for patients with a more acute/advanced form of the disease.
- To predict parkinson's disease, we can use the HOG image descriptor to quantify the input images and then train a Random Forest classifier on top of the extracted features.
### CODE 
- The dataset can be found at --> https://www.kaggle.com/kmader/parkinsons-drawings
- HOG will be used to quantify our image. HOG will naturally be able to quantify how the directions of a both spirals and waves change.And furthermore, HOG will be able to capture if these drawings have more of a “shake” to them, as we might expect from a Parkinson’s patient.
- Furthermore, Random Forest classifier can be trained on top of these extracted features.
- The output can be shown with the help of a montage using OpenCV.
- The output of training with WAVE dataset is -

 ![image](https://user-images.githubusercontent.com/63549553/134583851-b7205f68-7823-4ce0-8e84-d997bb5db355.png)
- 71.33% classification accuracy on the testing set, with a sensitivity of 69.33% (true-positive rate) and specificity of 73.33% (true-negative rate) was obtained with the WAVE data.

- The output of training with SPIRAL dataset is -

 ![image](https://user-images.githubusercontent.com/63549553/134584175-71a0540c-7860-4a1e-8b07-4a0a76440ea2.png)
- 80.67% accuracy on the testing set, with a sensitivity of 72.00% and specificity of 89.33% was obtained with the SPIRAL data.
### CONCLUSION 
- It can be inferred that for automatically detecting Parkinson’s disease using a dataset of hand drawn images, the SPIRAL data is more useful.
### ADDITIONAL RESOURCES
- More info about HOGs can be found at --> https://customers.pyimagesearch.com/lesson-sample-histogram-of-oriented-gradients-and-car-logo-recognition/
- Vector Normalizations in ML --> https://machinelearningmastery.com/vector-norms-machine-learning/
