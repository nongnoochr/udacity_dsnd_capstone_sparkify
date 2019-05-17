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

3. The [Sparkify.ipynb](./Sparkify.ipynb) notebook contains all steps in this process and markdown cells were used to assist in walking through the thought process for individual steps.

4. The [Sparkify.html](./Sparkify.html) was the report generated after running all cells in the notebook

## Results<a name="results"></a> 

1. There are noticable differences between a ratio of gender, average session time, and an average number of songs played within a single session  when comparing users who are churned and remain in service where:
    * Men have a much higher ratio to be churned
    * The average session time of users who remain in service is higher (303 minutes vs 283 minutes)
    * The average number of song per session of users who remain in service is higher (75 songs/session vs 70 songs/session)


2. A model trained from the Gradient-boosted tree classifier has a much better performance that a model trained form the Logistic Regression where the best model trained from the Gradient-boosted tree classifier achieved over 99% of area under ROC curve and has an accuracy over 97% while the best model trained from the Logistic Regression achieved only 70% of area under ROC and has an accuracy around 83%

The detailed findings and analysis can be found in a Medium post available [here](https://medium.com/@nongnoochroongpiboonsopit/supercharge-your-data-science-portfolio-with-pyspark-7811b7ae91de).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Data set used in this project was downloaded from the *Data Science Capstone Project:Using Spark to Predict Churn with Insight Data Science* of the ***[Data Scientist Nanodegree Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025)*** and must give credit to Udacity for the data.

This project is [MIT licensed](./LICENSE).