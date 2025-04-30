

# Face Recognition System

This project is a simple face recognition system built using Python and OpenCV. It performs two main tasks:
1. **Capturing Face Images**: It allows you to capture images of faces to create a dataset.
2. **Training the Model**: It uses the captured images to train a face recognition model.
3. **Recognizing Faces**: It can detect and recognize faces in real-time using a webcam.

## Project Structure

- `dataset/`: Folder to store captured face images.
- `trainer/`: Folder to store the trained model (`trainer.yml`).
- `haarcascade_frontalface_default.xml`: Pre-trained model for face detection (used by OpenCV).
- `face_recognition.py`: Script to capture face images and perform face recognition.
- `train_model.py`: Script to train the model from captured images.

## Installation

### Prerequisites

To run this project, you need to install the required libraries.

1. **Install Python**: Make sure Python 3.x is installed on your system.
2. **Install OpenCV**: You can install OpenCV using the following pip command:
   ```bash
   pip install opencv-python opencv-python-headless
   ```
3. **Install numpy**: Install numpy, which is needed for matrix operations:
   ```bash
   pip install numpy
   ```

4. **Install PIL (Pillow)**: To handle image processing:
   ```bash
   pip install pillow
   ```



## Usage

### Step 1: Capture Face Images

1. Run the `face_recognition.py` script to capture face images using your webcam.

   ```bash
   python face_recognition.py
   ```

2. The script will open your webcam and start detecting faces.
3. When a face is detected, it will capture the image and store it in the `dataset/` folder with filenames like `User.{id}.{sample_number}.jpg`.
4. Press 'q' to stop capturing images after you've captured enough images (e.g., 100 images for each person).

### Step 2: Train the Model

1. After capturing the images, run the `train_model.py` script to train the face recognition model.

   ```bash
   python train_model.py
   ```

2. The script will use the images in the `dataset/` folder to train the model.
3. Once the training is complete, the model will be saved as `trainer.yml` in the `trainer/` folder.

### Step 3: Recognize Faces

1. Run the `face_recognition.py` script again to recognize faces in real-time using your webcam.

   ```bash
   python face_recognition.py
   ```

2. The script will detect and recognize faces from the webcam feed.
3. It will display the recognized person's ID along with the confidence percentage on the screen.

### Step 4: Exit

- Press 'q' to exit the real-time recognition process.

## Notes

- Ensure that the `dataset/` folder contains images of people for training. The image filenames should follow the pattern `User.{id}.{sample_number}.jpg`, where `{id}` is a unique identifier for the person, and `{sample_number}` represents the image sequence (e.g., `User.1.1.jpg`, `User.1.2.jpg`, etc.).
- The trained model (`trainer.yml`) is saved in the `trainer/` folder. This model can be used for real-time face recognition.
- You can modify the face detection parameters and model to improve recognition accuracy.

## License

This project is open-source 
---

Let me know if you need any adjustments or additions to the README!