<div id="top"></div>

# Recognizing gender from voice using SVM
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

This work is about predicting a person's gender based on the sound characterstics.

## Table of contents
<ol>
  <li>
    <a href="#project-description">Project Description</a>
  </li>
  <li>
    <a href="#support-vector-machines">Support Vector Machines</a>
  </li>
  <li>
    <a href="#dataset-description">Dataset Description</a>
  </li>
  <li>
    <a href="#project-structure">Project Structure</a>
  </li>
  <li>
    <a href="#installation-&-setup">Installation & Setup</a>
  </li>
  <li>
    <a href="#results">Results</a>
  </li>
   <li>
    <a href="#contributions">Contributions</a>
  </li>
   <li>
    <a href="#contact">Contact</a>
  </li>
</ol>
<p align="right">(<a href="#top">back to top</a>)</p>

## Project Description
Support Vector Machine (SVMs) is one of the most powerful algorithms for problem solving in machine learning and is known to have deep roots in the fields of Statistical Learning Theory (SLT) and optimization problems along with numerous industrial applications. SVMs are known to reduce most of the problems in machine learning to optimization problems and the latter lies at the heart of SVMs. Due to its higher accuracy, support vector machine is a widely researched topic in the machine learning community. The algorithm promises a higher empirical performance. This project illustrates a detailed understanding of Support Vector Machines along with different parameters associated along with it. The accuracy scores were listed were displayed before and after hyperparameter tuning.
<p align="right">(<a href="#top">back to top</a>)</p>

## Support Vector Machines
SVM use supervised algorithms using support vector classifier as a base. The term support vector classifier is derived from the fact that all the observations on the edge and within the soft margins are called support vectors. It is one of the most important algorithms which are applicable for both classification as well as regression datasets. However, normally it is used for classification problems. The algorithm was first introduced in 1960 but it was Vapnik and his coworkers by the early 90s. This algorithm is extremely effective as it could handle numerous categorical and continuous variables.

Apart from machine learning, SVMs are also known to be effective in the domain of data mining. Numerous studies highlight the fact that SVMs are known to have significantly higher amount of accuracy as compared to other existing traditional classification algorithms. It is largely because they proceed with problem solving using finite training points and thus do not face the problems like overfitting, curse of dimensionality etc. It maps the training data in space to increase the separation between the categories. The newer data points would be mapped in the same space and would be predicted and placed in a category.

SVM supports both linear and non-linear classification. The latter is carried out by using kernel trick which simply means mapping the inputs in non-linear data into a higher-dimensional feature space.

The success of SVMs is mainly attributed to three fundamental reasons: Kernel trick, principle of maximal margin and dual theory. However, for some of the datasets, the values of cost and kernel parameters play a significant role in the accuracy of the model. Therefore, the user needs to continually perform considerable cross validation to obtain optimum parameter settings which in turn would result a higher accuracy score. Kernels are referred to as a core of SVM since they support a set of mathematical functions which are used for manipulation of data. In terms of real-time applications, SVMs are used in medical decision support, face authentication, image recognition, text categorization etc. SVMs are also applicable for all kinds of datasets be it, audio, video or text.

<p align="right">(<a href="#top">back to top</a>)</p>

## Dataset Description
This database was created to identify a voice as male or female, based upon acoustic properties of the voice and speech. The dataset consists of 3,168 recorded voice samples, collected from male and female speakers. The voice samples are pre-processed by acoustic analysis in R using the seewave and tuneR packages, with an analyzed frequency range of 0hz-280hz (human vocal range).

The following acoustic properties of each voice are measured and included within the CSV:

meanfreq: mean frequency (in kHz)<br />
sd: standard deviation of frequency<br />
median: median frequency (in kHz)<br />
Q25: first quantile (in kHz)<br />
Q75: third quantile (in kHz)<br />
IQR: interquantile range (in kHz)<br />
skew: skewness (see note in specprop description)<br />
kurt: kurtosis (see note in specprop description)<br />
sp.ent: spectral entropy<br />
sfm: spectral flatness<br />
mode: mode frequency<br />
centroid: frequency centroid (see specprop)<br />
peakf: peak frequency (frequency with highest energy)<br />
meanfun: average of fundamental frequency measured across acoustic signal<br />
minfun: minimum fundamental frequency measured across acoustic signal<br />
maxfun: maximum fundamental frequency measured across acoustic signal<br />
meandom: average of dominant frequency measured across acoustic signal<br />
mindom: minimum of dominant frequency measured across acoustic signal<br />
maxdom: maximum of dominant frequency measured across acoustic signal<br />
dfrange: range of dominant frequency measured across acoustic signal<br />
modindx: modulation index. Calculated as the accumulated absolute difference between adjacent measurements of fundamental frequencies divided by the frequency range<br />
Label: male or female<br />


The dataset could be downloaded using the [Link](https://www.kaggle.com/primaryobjects/voicegender)
<p align="right">(<a href="#top">back to top</a>)</p>

## Project Structure
  ├── Dataset/
      ├── voice.csv
  ├── SVM Explanation/
      ├── SVM_Outline.ipynb
      ├── images/
  ├── SVM_Gender_Recognition_from_Voice.ipynb
  ├── requirements.txt
  ├── .gitignore
  ├── img_temp/
<p align="right">(<a href="#top">back to top</a>)</p>

## Installation & Setup
1. Create a virtual environment in conda prompt using the following commands:
    * Make a virtual environment
 
      ```$ conda create -n [ENV_NAME] python=[PYTHON_VERSION]```
      <br>
      where ``ENV_NAME`` is the name of the virtual environment and ``PYTHON_VERSION`` is the version of python.
      
    * Activate the virtual environment
    
      ```$ conda activate [ENV_NAME]```
   
2. Add the virtual environment in the jupyter notebook using the following commands:
    * Install the ipykernel
    ```$ pip install --user ipykernel```

    * Manually add the kernel
    ```$ python -m ipykernel install --user --name=[ENV_NAME]```
    where ``ENV_NAME`` is the name of the virtual environment.
    
3. Install the requirements from requirements.txt:
    ```$ pip install requirements.txt```

4. Clone the project repo into the virtual environment
   
   ```$ git clone https://github.com/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine.git```
   
5. Execute the cells in the notebook ```SVM_Gender_Recognition_from_Voice.ipynb```.
<p align="right">(<a href="#top">back to top</a>)</p>

## Results
Voice based Gender Recognition was performed using SVM. In this work, a SDN specific dataset is used. The dataset originally includes 22 features. The output feature is the last column of the dataset i.e. Label which classifies the gender as male or female. After performing basic EDA process and applying the necessary feature selection techniques, an accuracy of 67.19% was observed. On tuning the hyperparameters using GridSearch, the accuracy rate increased significantly to 97.96% thereby displaying an increase of 45.79%.
<p align="right">(<a href="#top">back to top</a>)</p>

## Contributions
Contributions are what make open source such a fantastic environment to learn, inspire, and create. Any contribution you could provide to this existing work is much appreciated.
Please fork the repository or create a pull request if you have any suggestion for betterment. Subsequently, you could also open an issue for queries. Also, Don't forget to give the project a star!
<p align="right">(<a href="#top">back to top</a>)</p>

## Contact
&nbsp;<a href="anshumohanty2002@gmail.com"><img src="./img_temp/email.svg"></a>
&nbsp;&nbsp;<a href="https://github.com/AnshumanMohanty-2001"><img src="./img_temp/github.svg"></a>
&nbsp;&nbsp;<a href="https://www.linkedin.com/in/anshuman-mohanty-b21b04231/"><img src="./img_temp/linkedin.svg"></a>
<p align="right">(<a href="#top">back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine.svg?style=for-the-badge
[contributors-url]: https://github.com/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine.svg?style=for-the-badge
[forks-url]: https://github.com/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine/network/members
[stars-shield]: https://img.shields.io/github/stars/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine.svg?style=for-the-badge
[stars-url]: https://github.com/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine/stargazers
[issues-shield]: https://img.shields.io/github/issues/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine.svg?style=for-the-badge
[issues-url]: https://github.com/AnshumanMohanty-2001/Recognizing-Gender-by-voice-using-Support-Vector-Machine/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/anshuman-mohanty-b21b04231/
