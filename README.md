# PassivePy



Our aim with this work is to create a reliable (e.g., passive voice judgments are consistent), valid (e.g., passive voice judgments are accurate), flexible (e.g., texts can be assessed at different units of analysis), replicable (e.g., the approach can be performed by a range of research teams with varying levels of computational expertise), and scalable way (e.g., small and large collections of texts can be analyzed) to capture passive voice from different corpora for social and psychological evaluations of text. To achieve these aims, we introduce PassivePy, a fully transparent and documented Python library.

* * *
## Manual
### Step 1.
 Open your Python coding environment. We will use visual studio for this tutorial and suggest you install it too if you don’t already have a coding environment (link for installation). Make sure to install Python and Jupyter notebook by clicking on the Extensions icon (or ctrl + shift + x) and searching for python and Jupyter notebook.



### Step 2.
 In whatever coding environment you are, try creating a file. In Visual Studio, we right-click on the left side of the page and select “New File”. Type in the name and make sure to add “.ipynb” at the end.


![1](https://github.com/mitramir55/PassivePyWeb/blob/main/Images/1.jpg)



### Step 3.
Name this file whatever you’d like. Just make sure that you add “ipynb” at the end. Here, we name our file “tutorial.ipynb”.


![Image](https://github.com/mitramir55/PassivePyWeb/blob/main/Images/2-1.png)

### Step 4.
 As you can see a cell has appeared on the page for us to start our code. First, we have to make sure that your system has all the requirements needed for the analysis. These requirements have been previously collected in a file and all you need to do is use !pip install to install them. Along with these requirements, we use another line of code to install the package itself. For all this, you can just copy and paste the following two lines.



```
!pip install -r https://raw.githubusercontent.com/mitramir55/PassivePy/main/PassivePyCode/PassivePySrc/requirements_lg.txt
!pip install PassivePy==0.2.2
```

![Image](https://github.com/mitramir55/PassivePyWeb/blob/main/Images/2.png)


### Step 5.
After the code stops running you will see a message at the end of all the outputted text that says, “PassivePy has been successfully installed”. Then, we can easily import and initial the package with the following lines:
```
from PassivePySrc import PassivePy
spacy_model = "en_core_web_lg"
passivepy = PassivePy.PassivePyAnalyzer(spacy_model)
```


### Step 6.

 Sample Sentence Output: Now let’s experiment with PassivePy. Let’s say we have a sentence like “Natural resources are exhausted by humans.” And we would like to see if there’s any passive in this text. What we do is create a sample_text variable and input it to the function match_text of PassivePy. We want to see every type of passive, so we put True in front of truncated and full passive inside the brackets. 
 ```
sample_text = "Natural resources are exhausted by humans."
resutl_1 = passivepy.match_text(sample_text, full_passive=True, truncated_passive=True)
resutl_1
```