# udacity_dsnd_capstone_sparkify

##  Installation 

After cloning this repository, please unzip `mini_sparkify_event_data.json.zip` before running the `Sparkify.ipynb` notebook (I cannot directly upload the data to this repository due to a file size limitation in github)

Below are python libraries that are required to run this code using Python versions 3.*:
* pyspark 2.4.3*
* pandas 0.24.1
* matplotlib 3.0.2 
* seaborn 0.9.0 

(*) If you get an error complaining about an absence of Java when running [Sparkify.ipynb](./Sparkify.ipynb) on mac, follow the instructions below:

1. Install [pyspark](http://spark.apache.org/downloads.html) (I used [conda](https://anaconda.org/conda-forge/pyspark) to install it)
2. Install Java8 on your mac [link](https://helpx.adobe.com/x-productkb/global/install-java-jre-mac-os.html)

3. Open a new terminal and verify that Java is available on your mac by using the command below;
```
java -version
```

If you are seeing the message `No Java runtime present, requesting install.` (like what I saw when I installed Java on my mac), you will need to add the following export to your ~/.bash_profile (Refer to the top answer of [this stackoverflow post](https://stackoverflow.com/questions/44009058/even-though-jre-8-is-installed-on-my-mac-no-java-runtime-present-requesting-) )


```
export JAVA_HOME=/Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin/Contents/Home

```

4. Start a jupyter notebook in a brand new terminal to use the new environment setting

<hr />