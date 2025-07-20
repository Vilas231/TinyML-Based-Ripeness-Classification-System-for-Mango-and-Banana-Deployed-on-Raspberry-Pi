# TinyML-Based-Ripeness-Classification-System-for-Mango-and-Banana-Deployed-on-Raspberry-Pi
This project focuses on building an offline, real-time fruit ripeness classification system using TinyML, specifically targeting mangoes and bananas. The solution is designed to assist in reducing manual errors during ripeness detection by automating the process through image classification on a Raspberry Pi. The system uses two lightweight Convolutional Neural Network (CNN) models based on the MobileNetV2 architecture — one dedicated to mango classification (Raw, Ripe, Not a Mango) and the other for banana classification (Raw, Ripe).

Each model was trained on a dataset of over 3,000 images, enhanced through data augmentation techniques to improve generalization. Post-training, the models were quantized to TensorFlow Lite (TFLite) format to optimize them for edge deployment. The pipeline involves image capture via a Pi Camera, followed by HSV-based color segmentation to isolate the fruit from the background. The image is first passed through the mango classifier. If the result is "Not a Mango," it is redirected to the banana classifier for a secondary check.

The system operates fully offline and displays the output on a connected TFT screen, ensuring low-latency inference without relying on cloud resources. It achieved high classification accuracy — 99.30% for mango and 99% for banana — during testing.

The design is scalable and energy-efficient, making it suitable for deployment in agricultural fields, packaging centers, or embedded in portable devices like drones or ground rovers for autonomous crop monitoring.

