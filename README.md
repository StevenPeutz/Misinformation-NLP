# Masterthesis-Disinformation-NLP
A study comparing the robustness to MT induced noise of NLP based Disinformation Classification architectures (focussing on vectorization methods and  classification algorithm combinations).  
<br>
## About this project
This study uses a 6 x 7 x 4 design in terms of embeddings, models and testsets. Resulting in 42 NLP architectures, each tested on 4 noise<sup>1</sup> levels.   
<br>

**Embeddings:**
- CountVectorizer (BoW)
- HashingVector (HV)
- TF-IDF
- GloVe<sup>3</sup>
- Word2Vec<sup>4</sup> (w2v)
- FastText<sup>5</sup> (ft)
<br><br>

**Classification Models**
- Logistic Regression (LR)
- Naive Bayes (NB)
- Random Forest (RF)
- Support Vector Machine (SVM)
- K-Nearest Neighbour (KNN)
- GradientBoosting (GB)
- Extreme Gradient Boosting (XGB)   
  
<br>

Datasets:  

| Name                          | Rows   | Size (gzipped) | Storage | Download link (use raw version if directly in notebook)                                                   |
| -----------------------------|-------|----------------|---------| -------------------------------------------------------------------------------------------------------------|
| fake_train                    | 20.387| 38.4MB         | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/21k_Chendra/fake_train.csv.gz |
| fake_or_real_news             | 6.060 | 11.9MB         | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/6k_Jillani/fake_or_real_news.csv.gz |
| data                          | 6.241 | 4.7MB          | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/EUvsDisinfo.eu/data.csv.gz |
| monkeypox                     | 4.000 | 7.8MB          | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/MonkeyPoxMisinfo/monkeypox.csv.gz |
| Fake                          | 20.000| 23.7MB         | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/UVIC-ISOT/Fake.csv.gz |
| True                          | 20.000| 18.7MB         | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/UVIC-ISOT/True.csv.gz |
| CompiledDisinfo_74k<sup>1  </sup>          | 73.900| 75.1MB         | Github  | https://github.com/StevenPeutz/Masterthesis-Disinformation-NLP/blob/master/DATA/CompiledDisinfo_74k/CompiledDisinfo_74k.csv.gz | 


<br>
Embeddings:


|                Embedding               | Dims | Size (gzipped) |  Storage   |                                                 Download link                                                 |
| :------------------------------------|:----:|:--------------:|:----------:|:---------------------------------------------------------------------------------------------------------: |
|           GloVe  (50dim version)          | 50   |   66 MB        |   Kaggle   |         https://www.kaggle.com/datasets/stevenpeutz/tinypretrainedembeddings         |
|      FastText - Reduced (PCA)     | 50   |   240 MB       |   Kaggle   |         https://www.kaggle.com/datasets/stevenpeutz/tinypretrainedembeddings         |
|     Word2Vec - Reduced (PCA)       | 50   |   958 MB       |   Kaggle   |         https://www.kaggle.com/datasets/stevenpeutz/tinypretrainedembeddings         |


<br>
<br>
<sup>1  </sup> *Noise levels as introduced by machine backtranslations. 'N0' being the original testset (the version similar to training), 'N1' (1 level of backtranslation (EN -> RU -> EN), continuing to 'N3'.
For rough assessment of noise in a purely lexical sense, the Jaro-Winkler Distances (normalized) have been calculated and imported before and are imported in this notebook*  
<br>
<br>

