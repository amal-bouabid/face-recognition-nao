# face-recognition-nao

Computer vision and deep learning project for face recognition and human–robot interaction using FaceNet and MTCNN.

---

## Project Overview

This project implements a facial recognition pipeline designed for robotic interaction scenarios.

The system combines:

- Face detection using MTCNN
- Face alignment based on eye coordinates
- Deep feature extraction using FaceNet
- Face recognition using cosine similarity
- Embedding database generation for identity matching

The project was intended for integration with the NAO humanoid robot using NAOqi APIs for speech and robot interaction functionalities.

---

## Features

- Automatic face detection
- Face alignment and preprocessing
- Deep embedding extraction
- Facial identity recognition
- Embedding database generation
- Similarity-based matching
- Modular deep learning pipeline

---

## Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- FaceNet
- MTCNN
- NumPy
- Matplotlib
- NAOqi

---

## Project Structure

```text
face-recognition-nao/
│
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── train_model.ipynb
│   ├── alignment.ipynb
│   ├── embeddings_database.ipynb
│   ├── recognition.ipynb
│   └── utils.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## System Pipeline

- Dataset preprocessing and splitting
- Face detection using MTCNN
- Face alignment using eye coordinates
- Feature extraction using FaceNet embeddings
- Face classification and recognition
- Similarity comparison using cosine similarity

---

## Dataset Preparation

The preprocessing notebook automatically splits the dataset into:

- Training set
- Validation set
- Test set

using a 70/15/15 ratio.

---

## Model Training

The training pipeline uses:

- FaceNet pretrained architecture
- Transfer learning strategy
- TensorFlow/Keras framework
- Categorical classification for identity recognition

The model input size is:

```python
(160, 160, 3)
```

The FaceNet backbone is frozen during training and additional dense layers are added for classification.

---

## Recognition Pipeline

The recognition system performs:

1. Face detection using MTCNN
2. Face alignment based on eye positions
3. Embedding extraction using FaceNet
4. Cosine similarity computation
5. Identity matching with stored embeddings

---

## Embedding Database

Face embeddings are stored in a JSON database for identity matching and recognition.

Example:

```json
{
  "Person_Name": [embedding_vector]
}
```

---

## NAO Robot Integration

The project was designed for integration with the NAO humanoid robot using NAOqi APIs for:

- Speech interaction
- Human detection
- Interactive robotic behaviors

Due to compatibility limitations between NAOqi Python environments and modern deep learning libraries, the complete deployment on the physical robot was not fully finalized.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/amal-bouabid/face-recognition-nao.git
```

Move to the project directory:

```bash
cd face-recognition-nao
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

Run the notebooks in the following order:

1. `preprocessing.ipynb`
2. `train_model.ipynb`
3. `embeddings_database.ipynb`
4. `recognition.ipynb`

---

## Future Improvements

- Real-time webcam recognition
- Full deployment on NAO robot
- ROS2 integration
- Real-time human–robot interaction
- Improved database scalability
- Real-time streaming inference

---

## Notes

- The trained model weights (`.h5`) are not included in this repository due to file size limitations.

- The dataset used for training and evaluation is not publicly distributed for privacy and confidentiality reasons.

- Users can train the model using the provided notebooks and their own datasets.

- Some paths in the notebooks originally referenced Google Drive environments and may require adaptation to local paths.

---

## Author

**Amal Bouabid**

Engineering Degree in Industrial Computer Science  
Specialization: Control and Industrial Robotics

---

## License

This project is intended for academic and research purposes.
