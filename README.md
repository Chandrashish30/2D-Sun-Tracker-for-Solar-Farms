# 2 Axis Sun Tracker

## Motor Control System

This project implements a motor control system using an Arduino board and analog sensors to adjust the speed and direction of two motors. The system reads analog input values from four sensors (`topleft`, `topright`, `downleft`, `downright`) and adjusts the output pulse width modulation (PWM) signals to control two motors accordingly.

### Components Used

- Arduino Board
- Analog Sensors (connected to A0, A1, A2, A3)
- Two Motors (connected to PWM pins 9 and 10)

### Setup

1. Connect the analog sensors to the designated analog pins on the Arduino board.
2. Connect the motors to PWM pins 9 and 10 on the Arduino board.
3. Upload the provided Arduino sketch to the board.

### Sketch Explanation

The Arduino sketch sets up two PWM channels (`OCR1A` and `OCR1B`) to control the speed of two motors. The analog sensor readings determine the direction and magnitude of the adjustments made to the PWM signals.

- **topleft, topright, downleft, downright**: Variables storing analog sensor readings.
- **waittime**: Delay time used in the loop for gradual adjustments.
- **setup()**: Initializes the Arduino board, PWM channels, and sets initial values for `OCR1A` and `OCR1B`.
- **loop()**: Continuously reads analog sensor values and adjusts PWM signals to control motor speed and direction.

### Motor Control Logic

The motor control logic is based on comparing sensor readings and incrementing or decrementing the PWM values accordingly. The system also includes bounds checking to ensure that PWM values stay within acceptable ranges.

### Note

This README is a basic overview of the project. Additional information, such as circuit diagrams, physical connections, or specific use cases, may be necessary for a comprehensive understanding of the project.

Feel free to modify and enhance the code according to your specific requirements. For any issues or improvements, please open an issue or pull request on GitHub.

**Happy tinkering!**
