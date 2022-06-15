# Color-Detection-Python

Prerequisites

Before starting with this Python project with source code, you should be familiar with the computer vision library of Python that is OpenCV and Pandas.

OpenCV, Pandas, and numpy are the Python packages that are necessary for this project in Python.

The project folder contains 3 files:

    Color_detection.py – main source code of our project.
    Colorpic.jpg – sample image for experimenting.
    Colors.csv – a file that contains our dataset.
    How to run application on terminal.

Taking an image from the user

We are using argparse library to create an argument parser. We can directly give an image path from the command prompt/terminal.

 Next, we read the CSV file with pandas

The pandas library is very useful when we need to perform various operations on data files like CSV. pd.read_csv() reads the CSV file and loads it into the pandas DataFrame. We have assigned each column with a name for easy accessing.

Set a mouse callback event on a window

First, we created a window in which the input image will display. Then, we set a callback function which will be called when a mouse event happens.

Create the draw_function

It will calculate the rgb values of the pixel which we double click. The function parameters have the event name, (x,y) coordinates of the mouse position, etc. In the function, we check if the event is double-clicked then we calculate and set the r,g,b values along with x,y positions of the mouse.

Calculate distance to get color name

We have the r,g and b values. Now, we need another function which will return us the color name from RGB values. To get the color name, we calculate a distance(d) which tells us how close we are to color and choose the one having minimum distance.

Our distance is calculated by this formula:

d = abs(Red – ithRedColor) + (Green – ithGreenColor) + (Blue – ithBlueColor)

Display image on the window

Whenever a double click event occurs, it will update the color name and RGB values on the window.

Using the cv2.imshow() function, we draw the image on the window. When the user double clicks the window, we draw a rectangle and get the color name to draw text on the window using cv2.rectangle and cv2.putText() functions.

Run Python File

The beginner Python project is now complete, you can run the Python file from the command prompt. Make sure to give an image path using ‘-i’ argument. If the image is in another directory, then you need to give full path of the image.

