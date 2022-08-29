<h1 align="center"> Classification Capstone Project </h1>

<h2 align="center"> Coronary Heart Disease Risk Prediction </h2>

<p align="center"> 
  <img src="Image/heart.jpg" alt="heart.jpg">
</p>

![------------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

To predict coronary heart disease is considered one of the most difficult and complex tasks in the medical domain. On an average every minute a person dies due to "Coronary Heart Disease". In the domain of healthcare, data science is playing a vital role in analyzing massive amounts of data daily and taking out useful and valuable insights from the data to make the data valuable and make the medical domain more reliable and decrease the complexity of the process. Our study uses data processing techniques such as feature selection, data analysis and machine learning algorithms to forecast the likelihood of a heart disease and classify the patient's risk level. As a result, this document provides a comparative analysis of the performance of several machine learning methods and concludes the factors that affect the risk of ‘Coronary Heart Disease’.

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
