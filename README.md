<p align="center">
  <p align="center">
    <a href="https://justdjango.com/?utm_source=github&utm_medium=logo" target="_blank">
      <img src="https://assets.justdjango.com/static/branding/logo.svg" alt="JustDjango" height="72">
    </a>
  </p>
  <p align="center">
    The Definitive Django Learning Platform.
  </p>
</p>

---

# Django E-commerce

This is a static and simple e-commerce website built with Django.

## Quick demo

[![alt text](https://  .com/media/gifs/djecommerce.gif "Logo")]

---

## Project Summary

The website displays products. Users can add and remove products to/from their cart while also specifying the quantity of each item. They can then enter their address and choose Stripe to handle the payment processing.

[![alt text](https://justdjango.s3-us-west-2.amazonaws.com/media/thumbnails/djecommerce.png "Logo")](https://youtu.be/z4USlooVXG0)

---

## Running this project

To get this project up and running you should start by having Python installed on your computer. It's advised you create a virtual environment to store your projects dependencies separately. You can install virtualenv with

```
pip install virtualenv
```

Clone or download this repository and open it in your editor of choice. In a terminal (mac/linux) or windows terminal, run the following command in the base directory of this project

```
virtualenv env
```

That will create a new folder `env` in your project directory. Next activate it with this command on mac/linux:

```
source env/bin/active
```

Then install the project dependencies with

```
pip install -r requirements.txt
```

Now you can run the project with this command

```
python manage.py runserver
```

**Note** if you want payments to work you will need to enter your own Stripe API keys into the `.env` file in the settings files.

---

# Auto Attendance System by Face Recognition

Auto Attendance System using real time face recognition is designed to collect and manage student’s attendance records by taking pictures from camera devices installed in a class room. Based on the verification of students facial identification in the cameras, attendance will be updated in data base.


## Requirements & Libraries

* Desktop development with C++
* cmake
* dlib
* face_recognition
* numpy
* opencv-python
* tkinter
* sqlite3
## Detection & Recognition

Although many face recognition algorithms have been developed over the years, their speed and accuracy balance has not been optimal. But some recent advancements have shown promise. A good example is Facebook, where they are able to tag you and your friends with just a few images of training and with accuracy as high as 98%. So how does this work? Today we will try to replicate similar results using a face recognition library developed by Adam Geitgey. Let's look at the 4 problems he explained in his article.

#### Face recognition is a series of several problems:

* First, look at a picture and find all the faces in it
* Second, focus on each face and be able to understand that even if a face is turned in a weird direction or in bad lighting, it is still the same person.
* Third, be able to pick out unique features of the face that you can use to tell it apart from other people— like how big the eyes are, how long the face is, etc.
* Finally, compare the unique features of that face to all the people you already know to determine the person’s name.

#### Find Faces Locations and Encodings

We will use the proper functionality of the face recognition library. First, we will find the faces in our images. This is done using HOG (Histogram of Oriented Gradients) at the backend. Once we have the face they are warped to remove unwanted rotations. Then the image is fed to a pre-trained neural network that outputs 128 measurements that are unique to that particular face. The parts that the model measures are not known as this is what the model learns by itself when it was trained.

#### Compare Faces and Find Distance

Once we have the encodings for both faces, then we can compare these 128 measurements of these two faces to find similarities. Compare the package uses one of the most common machine learning methods linear SVM classifier. We can use the compare_faces function to find if the faces match. This function returns True or False. Similarly, we can use the face_distance function to find how likely the faces match in terms of numbers. This is helpful particularly when there are multiple faces to detect from.
## Screenshots

#### Home
![App Screenshot](https://github.com/sydtanvirali/Auto-Attendance-System-by-Face-Recognition/blob/main/Screenshots/homepage.jpg?raw=true)


