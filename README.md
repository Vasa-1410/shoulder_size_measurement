### MoveNet Shoulder Measurement Project
## Overview
This project aims to measure a person's shoulder width using the MoveNet model. The MoveNet model detects and outputs landmarks of a person's body, from which the distance between the left and right shoulders can be determined. By calibrating the pixel-to-distance ratio using the known average distance between two pupils, we can approximate the shoulder width in real-world units.

## Model
The MoveNet model used in this project is a lightweight model designed for single-person pose estimation. It detects key landmarks on a person's body, including shoulders, elbows, wrists, etc. The model can be accessed and downloaded from the following link: MoveNet Model.

## Methodology
* Landmark Detection: The MoveNet model is used to detect landmarks of a person's body, particularly focusing on the left and right shoulder landmarks.
* Shoulder Width Calculation: The Euclidean distance formula is applied to calculate the pixel distance between the left and right shoulder landmarks.
* Pixel-to-Distance Ratio: The distance between the pupils is measured in pixels using the MoveNet output. This value is then used to calculate the pixel-to-distance ratio by dividing the known average distance between two pupils (63mm) by the measured distance between the pupils in pixels.
* Shoulder Width Approximation: Finally, the pixel distance of the shoulder width is multiplied by the pixel-to-distance ratio to obtain the approximate shoulder distance in real-world units (e.g., millimeters).
Diagrammatic Representation

## Formulas
- ** Euclidean Distance Formula: \( d = \sqrt{{(x_2 - x_1)}^2 + {(y_2 - y_1)}^2} \)
- ** Pixel-to-Distance Ratio: \( \text{Pixel-to-Distance Ratio} = \frac{{\text{Average Distance Between Two Pupils}}}{{\text{Measured Distance Between Pupils in Pixels}}} \)
- ** Shoulder Width Approximation: \( \text{Shoulder Width (mm)} = \text{Pixel Distance of Shoulder Width} \times \text{Pixel-to-Distance Ratio} \)

### Use Cases
* Tailoring and Fashion Industry: Precise shoulder measurements are crucial for tailoring clothes to fit perfectly. This project can assist tailors and fashion designers in obtaining accurate shoulder width measurements.
* Health and Fitness: Shoulder width is an important parameter in fitness assessments and body measurements. This project can be used in fitness centers and health clinics for tracking body changes and progress.
* Virtual Fitting Rooms: Online retailers can utilize this project to provide virtual fitting rooms where customers can input their measurements for a more personalized shopping experience.
## Dependencies
* TensorFlow Lite: This project requires TensorFlow Lite for running the MoveNet model inference on various platforms.
* Python 3.x: The project is implemented in Python 3.x and requires Python environment setup.
Other dependencies: Check the requirements.txt file for additional dependencies.
