# AeroArt - Hand Gesture Based Drawing Application

## Project Overview

**AeroArt** is a real-time hand gesture-based drawing application that allows users to draw on a virtual canvas using just their hands. By leveraging computer vision and machine learning libraries, specifically **MediaPipe** for hand tracking, this project provides an innovative way to interact with digital content without the need for a physical pen or mouse. Users can switch between different colors, clear the canvas, and draw directly on the screen using their hand movements detected via a webcam.

## Features

1. **Hand Gesture Detection**: 
   - The application uses **MediaPipe's Hands** module to track and detect hand landmarks, enabling drawing with a forefinger and controlling functions with the thumb.
   
2. **Color Switching**: 
   - Users can choose from four different colors (Blue, Green, Red, and Yellow) by hovering their finger over the corresponding color buttons on the screen.
   
3. **Clear Canvas**: 
   - The "Clear" button allows users to reset the canvas and start fresh.
   
4. **Dynamic Drawing**: 
   - The application enables drawing in real time based on the user's hand movements, with the ability to continuously add new points as the hand moves across the screen.

5. **Webcam Integration**: 
   - AeroArt uses a webcam feed to detect hand gestures, meaning there’s no need for additional hardware beyond a camera.

## Libraries Used

- **OpenCV**: Used for real-time image capture and processing to display the webcam feed, draw shapes, and create the canvas interface.
- **NumPy**: Provides support for handling arrays and matrices, which is used to create the kernel for dilation and other image processing techniques.
- **MediaPipe**: Google's framework for machine learning applied to human body and hand tracking. Used here to detect hand landmarks and perform gesture-based interactions.
- **Collections**: The `deque` is used to manage points in a dynamic array structure, allowing the storage and management of multiple points for drawing with different colors.
  
## Watch the Demo Video

https://github.com/user-attachments/assets/f6d50e08-f2bd-4e5e-9f16-1406798bce87

## How It Works

1. **Hand Detection**: 
   - The **MediaPipe** model detects the hand landmarks in each frame captured from the webcam. Specific points on the hand (forefinger and thumb) are used to determine gestures for drawing or interacting with the virtual canvas.
   
2. **Drawing Mechanism**:
   - The position of the forefinger tip (landmark 8) is tracked, and its movement is used to draw lines on both the webcam feed and a separate virtual canvas.
   
3. **Color Selection and Clear Functionality**:
   - When the forefinger hovers over the designated areas for each color, the selected color is activated. 
   - Hovering over the "Clear" button allows the user to reset the canvas.

4. **Gesture Recognition**:
   - The relative positions of the forefinger and thumb are used to trigger specific actions like resetting the current points or adding new ones.

## User Interface

The application provides a basic user interface with buttons for color selection and canvas clearing. These buttons are displayed both on the webcam feed and the drawing canvas.

- **CLEAR**: Resets the canvas.
- **BLUE, GREEN, RED, YELLOW**: Change the drawing color.
  
The interface is intuitive, relying on simple hand gestures to control the drawing process.

## Usage Instructions

1. Clone the repository and navigate to the project directory.
   
2. Install the required dependencies:
   ```bash
   pip install opencv-python mediapipe numpy
   ```

3. Run the application:
   ```bash
   python aeroart.py
   ```

4. A window will open showing the webcam feed with buttons at the top. 
   - Move your forefinger over the "BLUE", "GREEN", "RED", or "YELLOW" areas to select a color.
   - Start drawing by moving your forefinger on the screen.
   - To clear the canvas, hover over the "CLEAR" button.

5. Press the `q` key to quit the application.



## Conclusion

**AeroArt** is a fun and interactive way to explore drawing using only hand gestures. By integrating cutting-edge hand tracking technology, it paves the way for more immersive and contactless user interfaces, and can be a stepping stone toward more complex gesture-based applications.

## Contact Information

For any queries or suggestions, please feel free to reach out:
- **Email**: mondalmrinal39@gmail.com
