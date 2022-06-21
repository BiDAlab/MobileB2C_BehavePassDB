# MobileB2C_BehavePassDB

**BehavePassDB_BehavePassDB** is a novel database of behavioral biometric data collected for typical mobile Human-Computer Interaction (HCI) activities. The database includes several **touch gestures (free-text keystroke, swipe, tap dynamics)**, and **background sensor data (accelerometer, gyroscope, magnetometer, lin. accelerometer, gravity sensor)** simultaneously acquired.

The database is used for the [IJCB 2022 Mobile Behavioral Biometric Competition (MobileB2C)](http://www.ijcb2022.org/#/competitions). More information about the competition is available [here](https://sites.google.com/view/mobileb2c/). The competition ended on June, 7th, 2022, but it will be soon established as an ongoing competition.

Contact: [mobileb2c.bidalab@gmail.com](mailto:mobileb2c.bidalab@gmail.com)


# **Data Format**

Each subject’s data are structured into 4 acquisition sessions. Each acquisition session contains different tasks (texting, text reading, gallery swiping, tapping). During each of the tasks, touchscreen and background sensor data are acquired.
The MobileB2C_BehavePass database will be divided into two subsets:
- Development: **MobileB2C_BehavePassDB DevSet** (51 users).
- Validation and Evaluation: **MobileB2C_BehavePassDB ValSet** and **MobileB2C_BehavePassDB EvalSet** (respectively 10 and 20 different users), including the skilled impostor case, i.e., along the 4 genuine sessions, 2 extra sessions carried out by a different user on the same mobile device are included. Such extra sessions will be used to verify a different user on the same mobile device as the genuine one.
 
Starting from the acquired raw data, both the development (MobileB2C_BehavePassDB DevSet) and the evaluation (MobileB2C_BehavePassDB EvalSet) databases will be provided in the form of JSON files structured as follows:
- **DevSet.json**, 51 users: Genuine sessions (“g1”-“g4”) : Tasks (“keystroke”, “readtext”, “gallery”, “tap”) : Modality (“touch”, “sensor_acc”, “sensor_accl”, “sensor_gyro”, “sensor_grav”, “sensor_magn”) : Time-Series Data
- **ValSet_Task_enrolment.json**: Pseudonymized Enrolment Sessions : Task : Modality (“touch”, “sensor_acc”, “sensor_accl”, “sensor_gyro”, “sensor_grav”, “sensor_magn”)  : Time-Series Data
- **ValSet_Task_verification.json**: Pseudonymized Verification Sessions : Task : Modality (“touch”, “sensor_acc”, “sensor_accl”, “sensor_gyro”, “sensor_grav”, “sensor_magn”)  : Time-Series Data. 
- **EvalSet_Task_enrolment.json**: Pseudonymized Enrolment Sessions : Task : Modality (“touch”, “sensor_acc”, “sensor_accl”, “sensor_gyro”, “sensor_grav”, “sensor_magn”)  : Time-Series Data
- **EvalSet_Task_verification.json**: Pseudonymized Verification Sessions : Task : Modality (“touch”, “sensor_acc”, “sensor_accl”, “sensor_gyro”, “sensor_grav”, “sensor_magn”)  : Time-Series Data. 

The Time-Series Data will be provided into a different form depending on the modality. Specifically, each acquired sample is structured as follows:
Keystroke data: \[timestamp, ascii_code\]

All other touch data: \[timestamp, x_coordinate / screen_width, y_coordinate / screen_height, action_type\]. action_type refers to the touch."0" corresponds to laying the finger, "1" to lifting the finger, "2" to moving the finger on the screen.

Background sensor data: \[timestamp, x_coordinate, y_coordinate, z_coordinate\]. 

The validation set labels are available upon [request](mailto:mobileb2c.bidalab@gmail.com).


# **Instructions for downloading MobileB2C_BehavePassDB**

1. Download your corresponding license agreement:

    [[link](http://atvs.ii.uam.es/atvs/licenses/MobileB2C_BehavePassDB_License.pdf)] Permanent researchers working at research or academic institutions.
    
    
    [[link](http://atvs.ii.uam.es/atvs/licenses/MobileB2C_Evaluation_License_ONLY_MobileB2C2022.pdf)] Selected companies and independent professionals generating research outcomes.
   

    Once the corresponding license agreement is signed, send the scanned copy to atvs@uam.es according to the instructions given in point 2.

2. Send an email to [**atvs@uam.es**](mailto:atvs@uam.es), as follows:

    _Subject:_ **[DATABASE download: MobileB2C_BehavePassDB]**

    Body: Your name, e-mail, telephone number, organization, postal mail, purpose for which you will use the database, time and date at which you sent the email with the signed license agreement.

1. Once the email copy of the license agreement has been received at ATVS, you will receive an email with a username, a password, and a time slot to download the database.
2. Download the [Development and Validation Set](http://atvs.ii.uam.es/atvs/intranet/free_DB/MobileB2C_BehavePassDB) and the final [Evaluation Set](http://atvs.ii.uam.es/atvs/intranet/free_DB/MobileB2C_BehavePassDB_EvalSet), for which you will need to provide the authentication information given in step 3. After you finish the download, please notify by email to [**atvs@uam.es**](mailto:atvs@uam.es) that you have successfully completed the transaction.
3. For more information, please contact: [**atvs@uam.es**](mailto:atvs@uam.es)


**A benchmark evaluation of user authentication performance based on MobileB2C_BehavePassDB is available in [\[1\]](https://arxiv.org/abs/2206.02502).**


# **REFERENCES**

[\[1\] G. Stragapede, R. Vera-Rodriguez, R. Tolosana, A. Morales, "BehavePassDB: Benchmarking Mobile Behavioral Biometrics", arXiv:2206.02502, 2022.](https://arxiv.org/abs/2206.02502)


