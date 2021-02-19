# apache-beam-python-GroupByKey
This repo is all about doing a GroupByKey transformation

<img src="https://avatars.githubusercontent.com/u/60019513?s=400&u=6601ccba9a28d0a3095067e657e7305603bd6dda&v=4" align="right"
     alt="Size Limit logo by Anton Lovchikov" width="110" height="120">
     
# Raju Nooka [![](https://img.shields.io/badge/Github-nrajubn)](https://github.com/nrajubn)

## Sub-topic : GroupByKey
- I have worked on "GroupByKey" for the file 'vgsales.csv' This dataset contains a list of video games with sales greater than 100,000 copies.
* The dataset, I have choosen is Kaggle. Here is the link [vgsales.csv](https://www.kaggle.com/gregorut/videogamesales)
* I have choosen the Google colaboratory to run the code.
- [My Google Colab Notebook on GroupByKey Transformation](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/GroupByKey.ipynb)
- Demonstration Video: []()
- My Personal Repo on apache beam python with README file - https://github.com/nrajubn/apache-beam-python-GroupByKey

## Prerequisites
- Python
- Apache beam
- Google Colab 

## Commands Used 
- First, install apache-beam using the below command.
```
!pip install --quiet -U apache-beam
```
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/apacheinstall.PNG)

- Install the other dependencies 
```
!pip install apache-beam[gcp,aws,test,docs]
```
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/dependencies.PNG)

- Program that performs the GroupByKey operation
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/code.PNG)

- output of the program
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/out.PNG)

- The command that lists all the files
```
! ls
```
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/list.PNG)

- First upload your .csv file to your google drive account.
- The email used should be same for both google drive and google Colab accounts.
- Import the .csv file run into google colab.
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/importfile.PNG)
```
# Code to read csv file into colaboratory:
!pip install -U -q PyDrive
from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive
from google.colab import auth
from oauth2client.client import GoogleCredentials
```
```
# Autheticate E-Mail ID
auth.authenticate_user()
gauth = GoogleAuth()
gauth.credentials = GoogleCredentials.get_application_default()
drive = GoogleDrive(gauth)
```

- To get the id of the file, right-click on the file in google drive account, select share link option, then copy the link.
- Remove the part that contains https://
- keep only the id part.

```
# Get File from Drive using file-ID
# Get the file
downloaded = drive.CreateFile({'id':'1b73yN7MjGytqSP5wimYAQmtByOvGGe8Y'}) # replace the id with id of file you want to access
downloaded.GetContentFile('superbowl-ads.csv') 
```

- Command to add the result to a output file
```
!cat output.txt-00000-of-00001 # output file
```
![](https://github.com/nrajubn/apache-beam-python-GroupByKey/blob/main/out.PNG)

## References 
- [Kaggle](https://www.kaggle.com/)
- [Apache-beam](https://colab.research.google.com/github/apache/beam/blob/master/examples/notebooks/get-started/try-apache-beam-py.ipynb)
- [link](https://medium.com/@selsaber/data-etl-using-apache-beam-part-one-48ca1b30b10a)



