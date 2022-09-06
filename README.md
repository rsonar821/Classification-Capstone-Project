<h1 align="center"> Classification Capstone Project </h1>

<h2 align="center"> Coronary Heart Disease Risk Prediction </h2>

<p align="center"> 
  <img src="Image/heart.jpg" alt="heart.jpg">
</p>

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

To predict coronary heart disease is considered one of the most difficult and complex tasks in the medical domain. On an average every minute a person dies due to "Coronary Heart Disease". In the domain of healthcare, data science is playing a vital role in analyzing massive amounts of data daily and taking out useful and valuable insights from the data to make the data valuable and make the medical domain more reliable and decrease the complexity of the process. Our study uses data processing techniques such as feature selection, data analysis and machine learning algorithms to forecast the likelihood of a heart disease and classify the patient's risk level. As a result, this document provides a comparative analysis of the performance of several machine learning methods and concludes the factors that affect the risk of ‘Coronary Heart Disease’.

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Problem Statement </h2>

The dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes. Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk factors.

The traditional risk factors for coronary heart disease are high LDL cholesterol, low HDL cholesterol, high blood pressure, family history, diabetes, smoking and being older than 45 for men.

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Features Used </h2>

<h3> Demographic: </h3>

* sex: Male or Female ("M" or "F")
* age: Age of the patient; (Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)
* education: Education level of a person

<h3> Behavioral: </h3>

* is_smoking: Whether or not the patient is a current smoker ("YES" or "NO")
* cigsPerDay: The number of cigarettes that the person smoked on average in one day. (Can be considered continuous as one can have any number of cigarettes, even half a cigarette.)

<h3> Medical (History): </h3>

* BPMeds: Whether or not the patient was on blood pressure medication (Nominal)
* prevalentStroke: Whether or not the patient had previously had a stroke (Nominal)
* prevalentHyp: Whether or not the patient was hypertensive (Nominal)
* diabetes: Whether or not the patient had diabetes (Nominal)

<h3> Medical (Current): </h3>

* totChol: Total cholesterol level (Continuous)
* sysBP: Systolic blood pressure (Continuous)
* diaBP: Diastolic blood pressure (Continuous)
* BMI: Body Mass Index (Continuous)
* heartRate: Heart Rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of a large number of possible values.)
* glucose: Glucose Level (Continuous)

<h3> Predict Variable (Desired Target): </h3>

* 10-year risk of coronary heart disease CHD (Binary: “1”, means “Yes”, “0” means “No”)

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Data Preprocessing </h2>

* The columns ‘cigsPerDay’, ‘education’, ‘BPMeds’, ‘totChol’, ‘BMI’, ‘heartRate’ and ‘glucose’ had missing (Nan) values but not much and were manageable.
* Imputed the missing values with the median of the respective columns for all the variables except ‘cigsPerDay’.
* The median of ‘cigsPerDay’ column was 0 but after checking the ‘is_smoking’ column found that the people has smoking habits, so imputed those Nan values with the mean of the column which was around 9.

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Exploratory Data Analysis </h2>

* High correlation found between systolic blood pressure and diastolic blood pressure and the relation is always collinear also according to the health science.
* Cigarette consumption per day was seen decreasing with increasing age.
* Increasing the cigarette consumption per day decreases the systolic blood pressure.
* Even if a person does not have a smoking habit but is greater in age, he/she can develop a risk of Coronary Heart Disease, so age plays a vital role in deciding the risk factor.
* Males smoke more as compared to females and thus are at a higher risk of Coronary Heart Disease.
* Even a person who is not medicated towards Blood Pressure still can get risky towards Coronary Heart Disease if cigarettes consumption per day is high.

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Handling Class Imbalance </h2>

To overcome this problem an oversampling technique known as SMOTE was being used. SMOTE is an oversampling technique where the synthetic samples are generated for the minority class. This algorithm helps to overcome the overfitting problem posed by random oversampling. It focuses on the feature space to generate new instances with the help of interpolation between the positive instances that lie together.

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Algorithms Used </h2>

1. Logistic Regression: 0.75
2. Decision Tree Classifier: 0.78
3. Random Forest Classifier: 0.94
4. Gradient Boosting Classifier: 0.89
5. XGBoost Classifier: 0.88
6. Support Vector Classifier: 0.81

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 align="center"> Conclusion </h2>

* Performed Hyperparameter Tuning using Randomized Search CV on Random Forest CLassifier.
* The Random Forest Classifier gave the best predictions out of all the other algorithms.
* The most important features for the model were found out to be 'age' and 'cigarettes per day'.
