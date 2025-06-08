# Student-Attendance-Management-System-Using-Facial-Recognition
This project developed a real-time student attendance management system using facial recognition, employing supervised machine learning algorithms like Haar Cascade and LBPH for accurate face detection, recognition, and efficient attendance tracking via a user-friendly GUI.

# Student Attendance Management System Using Facial Recognition

## Project Overview

This project implements a real-time **Student Attendance Management System** leveraging **facial recognition technology**. It provides an efficient and automated method for tracking student attendance in a classroom environment, aiming to replace traditional manual attendance systems. The system utilizes supervised machine learning algorithms for face detection and recognition, integrated within a user-friendly graphical interface.

## Key Features & Functionality

* [cite_start]**Real-time Facial Recognition:** Identifies and verifies student identities by matching faces from live camera feeds against a pre-existing database of student faces. 
* [cite_start]**Automated Attendance Marking:** Automatically records attendance based on successful facial recognition, minimizing manual effort and errors. 
* [cite_start]**User-Friendly GUI (Tkinter):** Features a graphical user interface developed with Python's Tkinter library for easy interaction, student registration, and attendance management. 
* [cite_start]**Face Detection & Feature Extraction:** Employs Haar Cascade classifiers for effective object (face) detection and extraction of discriminative facial features. 
* [cite_start]**Face Recognition Algorithms:** Utilizes the Local Binary Patterns Histograms (LBPH) Face Recognizer for robust and accurate facial recognition. 
* **Database Management (CSV & MySQL):**
    * [cite_start]Stores student details (Enrollment, Name, Date, Time) in CSV files (`StudentDetails.csv`). 
    * [cite_start]Supports creation of attendance tables in a MySQL database (`manually fill_attendance`, `Face_reco_fill`) for structured data storage. 
* [cite_start]**Manual Attendance Option:** Includes a feature to manually fill attendance for subjects, providing flexibility. 
* [cite_start]**Training Module:** Allows for training the facial recognition model by capturing multiple images of registered students. 
* [cite_start]**Attendance Export:** Converts attendance records into CSV format for easy viewing and record-keeping. 

## Technical Details & Methodology

* **Programming Language:** Python
* **Key Libraries & Modules:**
    * [cite_start]`OpenCV` (`cv2`): Essential for real-time video capture, image processing, face detection (`CascadeClassifier`), and facial recognition (`LBPHFaceRecognizer_create`). 
    * [cite_start]`Tkinter`: Standard Python interface for creating the GUI, handling user inputs, and displaying information. 
    * [cite_start]`NumPy`: Used for efficient numerical operations, particularly for handling image data as arrays (e.g., converting PIL images to NumPy arrays for processing). 
    * [cite_start]`Pandas`: Utilized for data manipulation, especially for reading student details from CSV and managing attendance dataframes. 
    * [cite_start]`csv`: Python's built-in module for reading from and writing to CSV files. 
    * [cite_start]`os`: Provides functions for interacting with the operating system, useful for file and directory management. 
    * [cite_start]`PIL` (Pillow): Python Imaging Library, used for image processing capabilities and handling image formats. 
    * [cite_start]`datetime` and `time`: For handling date and time stamps for attendance records. 
    * [cite_start]`pymysql.connections`: For connecting to and interacting with MySQL databases (e.g., creating tables, inserting data). 
    * [cite_start]`subprocess`: To open generated attendance sheets in file explorer. 

* **Facial Recognition Pipeline:**
    1.  [cite_start]**Image Acquisition:** Live video stream from a webcam is captured. 
    2.  [cite_start]**Grayscale Conversion:** Captured frames are converted to grayscale for efficient processing. 
    3.  [cite_start]**Face Detection:** Haar Cascade classifier identifies frontal faces within the grayscale image. 
    4.  [cite_start]**Feature Extraction & Training:** Detected faces are used to train the LBPH recognizer, creating a model (`Trainner.yml`) based on extracted features. 
    5.  [cite_start]**Face Recognition:** The trained model predicts the ID and confidence level of detected faces in real-time. 
    6.  [cite_start]**Attendance Recording:** If a face is recognized with sufficient confidence, the student's ID, name, date, and time are recorded. 

*(Note: Adjust file names and directory structure to match your actual project organization.)*

## Installation & Setup

1.  **Clone the repository:**
    `git clone https://github.com/your-username/student-attendance-system.git`
    `cd student-attendance-system`
2.  **Install Python dependencies:**
    `pip install opencv-python numpy pandas Pillow PyMySQL`
    *(Ensure you have Python 3 installed. Tkinter is usually built-in with Python installations.)*
3.  **Download Haar Cascade XML:**
    * Ensure `haarcascade_frontalface_default.xml` is in the correct directory (as specified in your code). You can typically find this in the OpenCV library's `data` folder.
4.  **MySQL Database Setup (Optional, for database logging):**
    * Set up a MySQL server.
    * Create a database (e.g., `manually fill_attendance`, `Face_reco_fill`) as per your script.
    * Update database connection details in `main_system.py` if necessary (host, user, password, db name).
5.  **Create necessary folders:**
    * `TrainingImage/`
    * `TrainingImageLabel/`
    * `StudentDetails/`
    * `Attendance/Manually Attendance/`
6.  **Run the application:**
    `python main_system.py`

## Usage

1.  **Register Students:** Use the "Take Images" option in the GUI to register new students by capturing their facial data.
2.  **Train Model:** After registering students, use the "Train Images" button to train the facial recognition model.
3.  **Mark Attendance:**
    * **Automatic:** Use "Automatic Attendance" to have the system recognize students and mark attendance from the live camera feed.
    * **Manual:** Use "Manually Fill Attendance" for manual entry of student attendance.
4.  **View Records:** "Check Sheets" allows you to view generated attendance CSV files. "Check Registered Students" gives access to the student details CSV.

## Author

Puneet Singh Arora
[LinkedIn Profile](https://www.linkedin.com/in/puneet-singh11/)
