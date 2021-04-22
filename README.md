# PatientDataGetter

# Team16_Capstone
This is a smartphone app design for personalized cancer symptom management. This application alerts users when it is time for their light therapy sessions, helping them more easily stick to a routine that works for them. Patient light therapy data, which includes therapy frequency and duration, is written from the app to a database that researchers from Michigan State University's College of Nursing can access.

![Visor Design](https://github.com/jkal90/Team16_Capstone/blob/44509c984a5c2b07154f853dfebe43d4ba560c9d/Visor%20Design.JPG)

The goal of this project is to design a smartphone application to help monitor and enhance observation of the prescribed light therapy. The application will be programmed for the time of the day the individual is advised to receive the light therapy. A text reminder will be sent through the app at the advised time of the day to notify the user. Real-time data will be provided by a timer that records start and end times of each light therapy session. If the user does not respond within 10 minutes of the advised time, a second text reminder will be sent, and if the user does not respond within 10 minutes of the second reminder, an alert message will be sent. This smartphone app will be programmed to notify and allow the user to record sleep/wake times, naptimes, and levels of fatigue each night for a pre-set timeframe. All the data collected by the application will be sent and stored in a server for future reference. This smartphone application will replace the previously used paper-pencil daily log.

*Development software used:*

The operating system used for the app is Android 11 and was designed using Android Studio. The backend was written using mostly Java 8 and the front end will be written using XML.  Information gathered by the app will be stored in a database hosted by the Michigan State University department of computer science.

## Data extraction for healthcare providers

The app writes to the database using a PHP script run through a student CSE Webdev account. None of the database information will need to be stored on the app or local storage, it will all be stored in the cloud. This is done to enhance security to mitigate source code being stored on apps across devices. The medical professionals will have a Python script that retrieves the data from the database and writes it to a CSV. This is also done by accessing the database through PHP.

### Python script for pulling data from a cloud-based .csv file into MS Excel

The python script **patient_data_getter.py** will be stored in a file location which is convenient to the healthcare provider. As long as the healthcare provider has the required software installed, they can generate Excel files with the necessary patient data. The Excel files will be created in the same file location that the **patient_data_getter.py** is saved in.

### Extracted database file format

A seperate Excel file is automatically generated for each database table that exists within the application. For example, a seperate Excel file will be generated for the bedtime questionnaire, the nap time questionnaire, the wake-up questionnaire, and timer usage.

### Required Software:

- .csv
- python
- MySQL Workspace
- MySQL Python Connector

### Install Python 3.7.9
Python 3.7.9 can easily be installed by visiting the link: https://www.python.org/downloads/release/python-379/
Choose from the following installer files that best suits your operating system and click through the easy to follow steps in the installation wizard:
![python 3.7.9](https://github.com/jkal90/Team16_Capstone/blob/bd88ce00d4ab12be2819d774233c7867a86cfb24/python379.JPG)

### Installing software from PowerShell terminal

1. Open Windows Powershell from the windows start menu
2. From command line enter the following commands

```
> mkdir patient_light_therapy [enter] 
# This creates a folder directory named "patient_light_therapy"

> cd .\patient_light_therapy\ [enter]
# This navigates you into the folder you had just created
 
> pip3 install mysql [enter]
> pip3 install mysql-connector [enter]
> pip3 install mysql-connector-python3 [enter]
> pip3 install requests [enter]
# You have now installed all the required software to run the patient_data_getter.py script
```

### Download the script

1. Open the following link: https://github.com/MaHuCS/PatientDataGetter
2. Download script by selecting the green "Code" button in the upper right and then selecting "Download ZIP"
![Screenshot of Download ZIP](https://github.com/jkal90/Team16_Capstone/blob/master/GithubScreenshot.png)

3. Extract the **patient_data_getter.py** from the ZIP and add it to the new folder you created
4. Now you may exit the windows powershell terminal and navigate to the folder you have created in the file explorer
5. You should see the script named **patient_data_getter.py**. To run the python script and generate excel files with the patient light therapy data, double-click **patient_data_getter.py** to run. The excel files should be generated in the same file location.

![patient data getter](https://github.com/jkal90/Team16_Capstone/blob/c4bee5952066fa59a2caf5a966f00a4b5a1489ea/patient_data_getter.jpg)

### How to Install App

**Download**

Download the app from the link using an Android device: https://github.com/MaHuCS/LightTherapyLog
![Android Studio download](https://github.com/jkal90/Team16_Capstone/blob/03ebb46d8923315c899568eb30cea44c938fd27b/ASdownload.JPG)

1. Download the APK from the link – you should then be able to see it downloading on the top bar of your device
2. Once it's downloaded, open Downloads, tap on the APK file, and tap Yes when prompted
3. The app will begin installing on the device
