# Rubiks-cube-mapper

In this project we built a Rubik’s Cube mapper using classic computer vision techniques.
<br> We converted the frames to HSV colors and then applied different masking techniques. Then, by using a global solution, i.e. prior knowledge of the color range we are able to identify the cube colors.
<br> We repeat the steps for each wig of the cube:
* **Calibrate the colors:**
We are saving the colors input from the user.
* **Find the cube contour and crop the frame:**
We apply a mask on a grayscale frame that enhances the black color in between the cube squares. Then, using the mask we find the cube contour and crop the frame.
* Apply color masks to HSV frames:
For each color, we create a mask of the color threshold. 
* **Find squares contours:**
Then we received a frame with 9 squares.
* **Classify the colors of the squares:**
For each square, we identify the color using the color threshold.
## Steps:
<img src="https://github.com/freddd1/Rubiks-cube-mapper/blob/main/media/algo.png" width="900" height="500" />

## Demo:

![Alt Text](https://github.com/freddd1/Rubiks-cube-mapper/blob/main/media/algo.gif)

## Instructions:

1. Run all the notebook and your webcam will open.
2. follow the written instructions. 
    1. find a good place to place the camera and the cube.
    2. Calibrate the colors by double clicking on the color on the screen
    3. Follow the printed instructions on how to rotate the cube
    4. If all went well you will see a printed version of the cube.
3. `active_cam` is the main function and has 1 parameter called `debug`.
    The default is `False`, but if `debug=True` you will see all of "behind the scene" screen and how the algorithm is actually working
4. If you want to recalibrate the colors you should restart the kernel and run all cells

## Notes:
1. In this project we used `python 3.7.7`, `numpy 1.18.5` and `cv2 4.4.0`
2. In order to use the code you should have a webcam and a Rubik's cube
