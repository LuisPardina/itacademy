# Lead Prediction for on-line courses 👩‍🎓

## Presentation of the chosen data set: 


X Education sells online courses to industry professionals. The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead.

Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%.



## General characteristics:

Dataset variables:

+ **Features**: the dataset contains 6 features in 6 columns, which are the measured parameters of the different sensors. These correspond to the vibrations detected in the rocket.

+ **Target**: The target corresponds to the label that classifies the types of states of the rocket according to the features measured by the sensors.

        - Target 0 corresponds to Stable
        - Target 1 corresponds to Light Turbulence
        - Target 2 corresponds to Moderate Turbulence
        - Target 3 corresponds to Severe Turbulence
        - Target 4 corresponds to Extreme Turbulence


## Presentation of the objectives 

X Education needs help in selecting the most promising leads, i.e. the leads that are most likely to convert into paying customers. The company needs a model wherein you a lead score is assigned to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance. The CEO, in particular, has given a ballpark of the target lead conversion rate to be around 80%.

![results](https://user-images.githubusercontent.com/97047277/175811421-086a3f1f-54e5-4065-8294-26a19424de8e.png)



## Requirements

This notebook requires a Python 3.6 or newer version. 

To run this notebook you must have installed the following libraries: 


        pip install pandas
        pip install numpy
        pip install matplotlib
        pip install seaborn
        pip install scipy
        pip install -U scikit-learn


For model selection we have used the Pycaret packacge: 


        pip install pycaret

This Pycaret package may be incompatible with some other components, so it is highly recommended to install it in a different environment.  See official website for more information: 

https://pycaret.gitbook.io/docs/



           

## Some additional considerations

Running the RandomSearch, GridSearch and CrossValidation sections of the notebook can take several minutes. The model is evaluated with several combinations of parameters and several different train and test partitions and this can take a long time to run.

## Acknowledgements

 For the preparation of this exercise, different online resources have been consulted: 

https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html


https://pycaret.gitbook.io/docs/


https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74


https://towardsdatascience.com/random-forest-hyperparameters-and-how-to-fine-tune-them-17aee785ee0d


https://www.analyticsvidhya.com/blog/2020/06/auc-roc-curve-machine-learning/




