Visual Guard
============

**Visual Guard** is a facial recognition system designed to securely identify students by comparing their faces against pre-stored data. Ideal for educational institutions and government agencies, Visual Guard enhances student authentication processes, offering real-time recognition and comprehensive student data verification.

Features
--------

*   **Facial Recognition**: Captures student faces via live camera or uploaded images and matches them with pre-registered data.
    
*   **Real-Time Processing**: Utilizes Flask-SocketIO for instant feedback and processing.
    
*   **Student Data Verification**: Matches faces with data fields like Name, Age, Registration Number, etc., stored in users.json.
    
*   **Flexible Image Input**: Accepts Base64-encoded images from cameras or file uploads.
    
*   **Optimized for Efficiency**: Fast image resizing and preprocessing for large images.
    
*   **Error Handling**: Returns specific error messages for failed image decoding, face detection, or recognition.
    

Technology Stack
----------------

*   **Flask**: Web framework for server-side operations.
    
*   **Flask-SocketIO**: Enables real-time server-client communication.
    
*   **face\_recognition (dlib)**: Library for face detection and recognition.
    
*   **OpenCV (cv2)**: For image processing.
    
*   **NumPy**: Image data handling.
    
*   **Pillow (PIL)**: Image manipulation.
    

System Workflow
---------------

1.  **User Data Initialization**: Loads student data and facial encodings from users.json.
    
2.  **Real-Time Image Processing**: Processes submitted images, resizing them and extracting face encodings.
    
3.  **Identity Verification**: Compares face encodings with stored data to confirm identity.
    
4.  **Response to Client**: Returns the student profile or an error message in real-time.
    

Installation and Setup
----------------------

### Prerequisites

*   **Python 3.12**
    
*   **pip** for installing dependencies
    

### Installation Steps

1.  bashCopy code
```
  git clone cd visual-guard
```
    
3.  bashCopy code
```
pip install -r requirements.txt
```
    
3.  **Prepare User Data**:
   Add student details in users.json. Include paths to student images.
    
4.  Run the Application:
```
python app.py
```
    

Sample users.json Structure
---------------------------

json
```
{
  "Name": "L",
  "Age": 19,
  "Designation": "Student",
  "Registration No.": "PT22CS092"
}
```

Error Handling
--------------

*   **Invalid Image Format**: "Failed to decode image."
    
*   **No Face Detected**: "No face found in the image."
    
*   **Recognition Failure**: "Could not encode face features."
    
*   **No Match**: "No match found in database."
    

Future Enhancements
-------------------

*   Centralized student databases
    
*   Enhanced AI-based recognition
    
*   Mobile and cloud integration
    

Documentation
-------------

For detailed project documentation, click here.
