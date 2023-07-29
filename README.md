# Calf Sounds Data Analysis
#### Análise de dados de sons de bezerros - [Clique aqui para versão PT-BR](https://github.com/geangobo/calf_sounds_data_analysis/blob/main/readme_PT_BR.md) 


Analysis of bovine sound data, project titled "Standardization of dairy calves' vocalization," developed in partnership with the University of São Paulo (EESC-USP) and the University of São Paulo (ESALQ-USP), aiming to search for patterns in the vocalizations of the calves using Machine Learning techniques.

## ❗ Question problem
In animal science, the importance of animal vocalization is well known; however, little is explored regarding the composition of each sound and its relation to animal welfare. Therefore, we seek patterns by analyzing features extracted from sound data, using specialized libraries for audio analysis and processing (Librosa).

## 🔊 Data Collection:
The audios were recorded on a farm with a controlled environment, using professional audio recording equipment.

## 🚀 Challenge:
Database with scarce data, Data Augmentation was applied to the audios in order to increase the robustness of the audios and the accuracy of the Machine Learning model to search for patterns.

## 💾 Database:
The [audio](dados.audio.com) database contains animal vocalizations, organized into vocalizations from July and November, following a naming convention:

"***animalID_breastfeeding_DayMonthYear_***"

Concepts of Animal Science:

pm --> Pre-suckling

dm --> Post-suckling

#### ex:
- *01_dm_manha_100722.wav* --> Animal 01 Post-weaning on July 10, 2022

Furthermore, the database contains the [dataframes](dataframe.com) with the 11 features extracted from the audios, separated by each animal group, date, and condition (pm or dm). 
### Data augmentation
Data augmentation techniques were applied, and the **features were extracted considering the augmented sound data**, which are labeled with "aumentado" (meaning "augmented" in PT-BR) at the end of the folder name. The Data Augmentation techniques were adapted to work with sound and have the same effect as when applied to images. Therefore, for the sounds, we applied the following techniques: 
  
- Addition of random noise
- Change of pitch
- Time shifting


## 📋 Project Prerequisites: 
- Jupyter Notebook (Python 3)
- Librosa
- Pandas
- Mosqito
- SciPy
- Scikit-learn
- Seaborn
- Matplotlib
  
🔧[Access requirements.txt for installation](link.aqui_da_parte_de_requisitos.com)
## 📊 Extracted features for evaluation:
- Mean FFTs (Fast Fourier Transform) 
- Max FFT’s (Fast Fourier Transform)
- Loudness
- Envelopes - five histograms of data
- Roughness 
- Sharpness
- Spectrogram

*With that, 11 features will be extracted from the audios using audio analysis and processing libraries. The features will be processed through classification algorithms to select the best features for the model.*

## 🤖 Main classifiers from Scikit-learn used in the project: 
- [Random Forest (RN)](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html#sklearn.ensemble.RandomForestClassifier)
- [K-Nearest Neighbors (KNN)](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html#sklearn.neighbors.KNeighborsClassifier) 
- [Support vector machine (SVM)](https://scikit-learn.org/stable/modules/svm.html#svm-classification)

 ## 🤝 Contributors: 
 - PhD. Maíra Martins da Silva (EESC-USP)
 - PhD. Iran José Oliveira da Silva
 - M.Sc Karen Airosa Machado de Azevedo

  
