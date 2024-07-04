# PQ event toolbox


### This toolbox provides a versatile collection of tools designed specifically to create robust and varied datasets used in the evaluation and testing of machine learning and deep learning algorithms. 
### Is a usefull tool for researchers, data scientists, and developers who need synthetic or custom datasets that reflect different scenarios and distributions for analysis and model development.



**Key Features:**

+ **Synthetic Data Generation:** Enables the creation of artificial data based on predefined PQ events. This facilitates the creation of customized datasets with specific characteristics.
  
+ **Dimensionality and Complexity Control:** Provides options to adjust data dimensionality, complexity of relationships between variables, and the presence of noise or outliers, enabling comprehensive testing of algorithms.
  
+ **Automatic Labeling**: Offers capabilities for automatically labeling generated datasets according to predefined rules  streamlining the data preparation process for model training and validation.
  
+ **Integration with ML Frameworks:** Compatible with major machine learning frameworks such as TensorFlow, PyTorch, scikit-learn, among others, facilitating seamless integration of generated datasets into development and experimentation pipelines.
  
+ **Visualization and Exploratory Analysis:** Includes tools for visualizing and performing exploratory analysis of generated datasets, allowing for a deep understanding of data characteristics and distributions before their use in machine learning models.

 This toolbox let you generate and visualize up to 28 power quality events and let you modify caracteristics realted to each one of them.
 
> ![Principal](https://github.com/Micke1995/ROPEC-2024/blob/main/Figures/Principal.png)

Also you can visualize a Fourier spectrum related to the signal.
>![FFT](https://github.com/Micke1995/ROPEC-2024/blob/main/Figures/FFT.png)

The toolbox let you generate and save custmons datasets.

> ![Export](https://github.com/Micke1995/ROPEC-2024/blob/main/Figures/Export.png) 

Also you can load a Machine Learnig model or a Deep learning model and predict the signal is generated by the PQ event generator.

>![Predict](https://github.com/Micke1995/ROPEC-2024/blob/main/Figures/PredictML.gif)

In this repository there are 2 models that you can load and use.

+ The first model is a decision tree the model was trained and tested with the following signals and got this results:

  >![BarDT](https://github.com/Micke1995/ROPEC-2024/blob/main/Figures/barplot_DecisionTree.png) 

+ The second model is a Support Vector Machine the model was trained and tested with the following signals and got this results:

  >![BarSVM](https://github.com/Micke1995/ROPEC-2024/blob/main/Figures/barplot_SVM.png) 

# Note:
+ All the machine lerning models recive the signal from the funcion FeatExtraction() that is contained in Tools.py this function made a feature extraction and return a vector with 6 features :
  - RMS or mean value 
  - Imin local minimal of the signal
  - Imax local maximal of the signal
  - Nlm Number of local maximal
  - Zc Number of zero crossing
  - Energy
+ All the deep learning models recive the raw signal, without feature extraction.
+ The PQ model should be inizialed with the same values of Fundamental Frequency, Sampling rate and Event length that the Machine Learning Model was trained.


#Getting started with Anaconda3:

1.Install Anaconda3 on your machine
2.Clone this repository
3.Navigate to this repository in your terminal
4.Create an environment using the following command (for Mac/Linux use the generic terminal, for Windows, you can use the Anaconda prompt terminal)
  +Run conda env create -f environment.yml in your terminal
5.Activate the environment by running conda activate tf
6.Run the app by triggering the python file python GUIFN.py
