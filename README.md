# voice-assitant-for-blind-people

# Overview

This project aims to empower visually impaired individuals by providing them with a voice-enabled assistant that can identify and describe objects in their surroundings. Utilizing TensorFlow Lite, Python, and Raspberry Pi, this solution leverages image classification techniques to deliver real-time feedback, enhancing the independence and mobility of users.

![WhatsApp Image 2024-07-25 at 815](https://github.com/user-attachments/assets/1e3aa03a-0419-4475-b3ff-fbcc8e284ebc)


# Features

* Image Classification : Utilizes pre-trained models to classify objects in real-time through the camera.
* Voice Feedback: Converts the classification results into audible descriptions, allowing users to understand their environment.
* Lightweight and Efficient: Built with TensorFlow Lite to ensure smooth performance on Raspberry Pi devices.
* User-Friendly Interface: Simple and intuitive commands for easy interaction.

# Technology Stack

* Raspberry Pi: A low-cost, credit-card-sized computer that can be used for various DIY projects.
* TensorFlow Lite: A lightweight version of TensorFlow designed for mobile and edge devices, enabling efficient model inference.
* Python: The programming language used to implement the system's logic and handle interactions.
* OpenCV: A library for image processing that helps in capturing and processing images from the camera.

# How It Works

![image(0)](https://github.com/user-attachments/assets/00fc3387-b7e8-49f3-b918-02ce4c283b76)

* Image Capture: The Raspberry Pi camera module captures live video frames.
* Object Detection: Each frame is processed using a TensorFlow Lite model that identifies various objects.
* Voice Output: The identified objects are converted into speech using a text-to-speech engine, providing users with immediate feedback about their surroundings.

```pycon
    if detection_result_list:
        for result in detection_result_list:
            for detection in result.detections:
                for category in detection.categories:
                    
                

                    print(f" Category Name - {category.category_name}")


                    engine.say(category.category_name)
                    engine.runAndWait()
                    engine.stop()
                    time.sleep(1)
```
