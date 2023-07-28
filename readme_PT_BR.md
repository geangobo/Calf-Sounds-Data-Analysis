# Análise de dados de sons de bezerros

Análise de dados de sons de bovinos, projeto com título “Padronização da vocalização de bezerros leiteiros”, desenvolvido em parceria com a Universidade de São Paulo (EESC-USP) e Universidade de São Paulo (ESALQ-USP) visando buscar padrões nas vocalizações dos bezerros utilizando técnicas de Machine Learning. 

## ❗ Situação problema
Na ciência animal sabe-se a importância da vocalização do animal, porém, pouco é explorado a respeito da composição de cada som e a relação com bem estar animal. Com isso, buscamos os padrões analisando as features extraídas dos dados de sons, usando bibliotecas próprias para análise e processamento de áudio (Librosa).

## 🔊 Coleta dos dados:
Os áudios foram gravados em uma fazenda com ambiente controlado, utilizando equipamentos profissionais de gravação de áudios.

## 🚀 Desafio:
Database com dados excassos, foi aplicado Data Augmentation nos áudios com a finalizade de aumentar a roustez dos áudios e a precisão do modelo de Machine Learning para buscar padrões.

## 💾 Banco de dados:
O banco de dados de [áudio]([dados.audio.com](https://github.com/geangobo/calf_sounds_data_analysis/tree/main/Database/sound_database)) contém as vocalizações dos animais, sendo organizado em vocalizações de julho e novembro, seguindo a seguinte regra de nomenclatura:

***Numero do animal_mamada_DiaMesAno***

Conceitos zootécnicos:

pm --> Pré-mamada

dm --> Pós-mamada

#### ex:
- *01_pm_manha_100722.wav* --> Animal 01 Pós-mamada dia 10 de julho de 2022.

Além disso, o banco de dados contém os [dataframes](banco.com) com as 11 features extraídas dos áudios, sendo separada por cada grupo de animal, data e estado (pm ou dm). 

### Data augmentation
Foi aplicado técnicas de aumento de dados, as **features foram extraídas considerando os dados de sons com aumento** que estão com nome "aumentado" no final do nome da pasta. As técnicas de Data Augmentation foram adaptadas para trabalhar com som e ter o mesmo efeito que quando usado em imagens, desse modo, no sons aplicamos:
  
- Adição de ruído aleatório
- Mudança de tom
- Deslocamento de tempo


## 📋 Pré-requisitos do projeto: 
- Jupyter Notebook (Python 3)
- Librosa
- Pandas
- Mosqito
- SciPy
- Scikit-learn
- Seaborn
- Matplotlib

🔧[Acesse requirements.txt para instalação](link.aqui_da_parte_de_requisitos.com)
## 📊 Features extraídas para avaliação:
- Média FFT’s (Transformada rápida de Fourier) 
- Máxima FFT’s (Transformada rápida de Fourier)
- Sonoridade (loudness) 
- Envelopes – cinco histogramas de dados
- Rugosidade  
- Nitidez
- Espectrograma

*No total serão 11 features extraídas dos áudios usando as bibliotecas de análise e processamento de áudio. As features serão processadas em algoritmos de classificação para ser escolhido as melhores features para o modelo.*

## 🤖 Principais Classificadores do Scikit-learn usados no projeto: 
- [Random Forest (RN)](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html#sklearn.ensemble.RandomForestClassifier)
- [K-Nearest Neighbors (KNN)](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html#sklearn.neighbors.KNeighborsClassifier) 
- [Support vector machine (SVM)](https://scikit-learn.org/stable/modules/svm.html#svm-classification)


