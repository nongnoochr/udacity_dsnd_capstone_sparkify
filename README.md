### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [Files Description](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

##  Installation<a name="installation"></a>

The data file `mini_sparkify_event_data.json.zip` must be unzipped before running the `Sparkify.ipynb` notebook

Below are python libraries that are required to run this code using Python versions 3.*:
* pyspark 2.4.3
* pandas 0.24.1
* matplotlib 3.0.2 
* seaborn 0.9.0 

*[TROUBLESHOOTING on MAC]* If you get an error complaining about an absence of Java when running [Sparkify.ipynb](./Sparkify.ipynb) on mac, follow the instructions below:

1. Install [pyspark](http://spark.apache.org/downloads.html) (I used [conda](https://anaconda.org/conda-forge/pyspark) to install it)
2. Install Java8 on your mac [link](https://helpx.adobe.com/x-productkb/global/install-java-jre-mac-os.html)

3. Open a new terminal and verify that Java is available on your mac by using the command below:
```
java -version
```

If you are seeing the message `No Java runtime present, requesting install.`, you would need to add the following export to your ~/.bash_profile 
(Please refer to the top answer of [this stackoverflow post](https://stackoverflow.com/questions/44009058/even-though-jre-8-is-installed-on-my-mac-no-java-runtime-present-requesting-) )


```
export JAVA_HOME=/Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin/Contents/Home

```

4. Start a jupyter notebook in a brand new terminal to use the new environment setting

## Project Motivation<a name="motivation"></a>

For this project, I was interestested gaining experience with using [Spark](https://databricks.com/spark/about) to
1. Perform the Exploratory Data Analysis (EDA) with large and realistic datasets.
2. Perform the Machine Learning process with Spark including Feature Creation, Model Training, Hyperparameter Tuning.

More specifically, I was interested in learning how to use Spark to manipulate large and realistic datasets with Spark to engineer relevant features for predicting churn, and also use Spark MLlib to build machine learning models with large datasets which is far beyond what could be done with non-distributed technologies like scikit-learn.


## Files Description<a name="files"></a>
1. The data file `mini_sparkify_event_data.json.zip` must be unzipped before running the notebook.

2. This data set `mini_sparkify_event_data.json` is a mini subset (128MB) of the full dataset available (12GB)

2. The [Sparkify.ipynb](./Sparkify.ipynb) notebook contains all steps in this process and markdown cells were used to assist in walking through the thought process for individual steps.


## Results<a name="results"></a> 

The main findings of the code can be found at the post available [here](xxx).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Data set used in this project was downloaded from the *Data Science Capstone Project:Using Spark to Predict Churn with Insight Data Science* of the ***[Data Scientist Nanodegree Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025)*** and must give credit to Udacity for the data.

This project is [MIT licensed](./LICENSE).