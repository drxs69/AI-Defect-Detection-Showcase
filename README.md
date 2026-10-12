# 🔍 AI-Powered Defect Detection System

### Computer Vision · Microservices · Containerisation · Kubernetes

**Project Type:** Academic Team Project

**Technologies:** Python · TensorFlow · MobileNetV2 · REST APIs · Docker · Kubernetes · SQLite

🔗 [Original Team Repository](https://github.com/JavierTanHL/EGT307_Project)

---

## 📖 Project Overview

Developed as part of a team project, this system uses computer vision and machine learning to classify captured product images as `GOOD` or `BAD`.

The application consists of four independent microservices responsible for web interactions, model inference, data storage and model training.

The project explores how machine learning can be integrated into a modular, containerised application that supports scalable deployment.

---

## 🎯 Project Objectives

- Develop a browser-based interface for capturing product images.
- Perform image classification using trained machine learning models.
- Store inspection records and captured images for future reference.
- Separate system responsibilities using microservices.
- Deploy the application using Docker and Kubernetes.

---

## 🏗️ System Architecture

```text
               Browser / Webcam
                       |
                       v
               Web/API Service
                   Port 8000
                       |
              +--------+--------+
              |                 |
              v                 v
       Inference Service   Storage Service
          Port 8001          Port 8002
              |                 |
         TensorFlow         SQLite Database
           Models           & Saved Images
              ^
              |
       Trainer Service
          Port 8003
```

The Web/API service handles user interactions and coordinates inference and storage operations.

The Inference service loads trained models and returns classification predictions.

The Storage service maintains inspection history and captured images.

The Trainer service enables new item-specific models to be trained and loaded without redeploying the entire application.

---

## 👨‍💻 My Contributions

Although the project was developed collaboratively, I was involved in implementing and integrating several components beyond my formally assigned responsibilities.

My primary involvement included:

- Contributing to the development of the Web/API, Inference and Storage microservices.
- Integrating API communication and data flow between services.
- Troubleshooting service integration and application functionality.
- Participating in implementation, testing and debugging.

The project's official service ownership and team credits remain documented in the original repository.

---

## ⚙️ Technical Highlights

### 1. Computer Vision and Inference

The application uses TensorFlow-based image classifiers to predict whether a captured product is classified as `GOOD` or `BAD`.

Images are processed into a consistent 224 × 224 input format before inference.

### 2. Microservices Architecture

Four independent services separate application responsibilities.

This architecture supports modular development, independent deployment and service-level troubleshooting.

### 3. Docker Containerisation

Docker Compose allows the services to run together within a reproducible containerised environment.

### 4. Kubernetes Deployment

The system supports Kubernetes deployment using Minikube.

The Inference service can be scaled independently, including through a Horizontal Pod Autoscaler configured for CPU utilisation.

### 5. Model and Data Persistence

SQLite stores inspection records, while persistent volumes support application data, trained models and training datasets.

---

## 🚧 Challenges and Lessons Learned

### Service Integration

Connecting several independently running services required careful coordination of API communication, request handling and error management.

### Containerised Deployment

Working with Docker and Kubernetes improved my understanding of container networking, service deployment and infrastructure configuration.

### Machine Learning Limitations

The system performs whole-image binary classification rather than locating individual defects.

Model predictions can also be affected by differences between training images and real-world webcam conditions.

---

## 📸 Demonstration

*Add actual screenshots or a short recorded demonstration showing:*

- Web interface and image capture
- Classification results
- Inspection history
- Running Docker containers
- Kubernetes deployment and scaling

---

## 💡 Key Learning Outcomes

This project strengthened my understanding of:

- Designing and integrating distributed software components.
- Developing applications around machine learning models.
- Using REST APIs for inter-service communication.
- Deploying containerised applications.
- Debugging and testing interconnected systems.
- Collaborating on larger software engineering projects.

---

## 👥 Project Credits

This project was developed collaboratively by the EGT307 project team.

Official service responsibilities and source code are documented in the [original team repository](https://github.com/JavierTanHL/EGT307_Project).

This showcase describes my personal involvement and technical learning from the project.
