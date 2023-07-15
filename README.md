# Robotic Arm Vehicle 

![visits](https://visit-counter.vercel.app/counter.png?page=https%3A%2F%2Fgithub.com%2FPrakasRavichandran%2Frobotic-arm-vehicle&s=40&c=00ff00&bg=00000000&no=2&ff=digi&tb=&ta=)

This repository contains the code for an automation vehicle equipped with a robotic arm powered by hydraulic actuators, designed for sewage cleaning applications. The vehicle is capable of remote control through a Bluetooth module and is equipped with Mecanum wheels for easy maneuverability.

## Components Used

- Arduino board (compatible with the selected libraries)
- HC-05 Bluetooth module for remote control
- Servo motors for the robotic arm (servo01, servo02, servo03, servo04, servo05, servo06)
- AccelStepper library for controlling the Mecanum wheels
- SoftwareSerial library for Bluetooth communication
### Setup Instructions

1. Connect the hardware components as follows:
   - Connect the Bluetooth module to Arduino's RX (A8) and TX (38) pins.
   - Connect the servo motors to the appropriate digital pins (servo01: 5, servo02: 6, servo03: 7, servo04: 8, servo05: 9, servo06: 10).
   - Connect the hydraulic actuators to the respective digital pins (LeftBackWheel: 42, 43; LeftFrontWheel: 40, 41; RightBackWheel: 44, 45; RightFrontWheel: 46, 47).

2. Install the required libraries:
   - SoftwareSerial: [Download the library](https://www.arduino.cc/en/Reference/SoftwareSerial) and follow the installation instructions.
   - AccelStepper: [Download the library](https://www.arduino.cc/reference/en/libraries/accelstepper/) and follow the installation instructions.
   - Servo: This library is pre-installed with the Arduino IDE.

3. Upload the code to the Arduino board using the Arduino IDE.

4. Power on the robotic arm vehicle and establish a Bluetooth connection with a compatible device (e.g., smartphone).

### Usage

Once the robotic arm vehicle is powered on and the Bluetooth connection is established, you can send commands to control its movements and the robotic arm. Here are the available commands:

- `0`: Stop all movements.
- `1`: Move the vehicle forward.
- `2`: Move the vehicle backward.
- `3`: Move the vehicle right forward.
- `4`: Move the vehicle left forward.
- `5`: Move the vehicle sideways right.
- `6`: Move the vehicle sideways left.
- `7`: Move the vehicle right backward.
- `8`: Move the vehicle left backward.
- `9`: Rotate the vehicle to the left.
- `10`: Rotate the vehicle to the right.
- `11`: Save the current position of the robotic arm.
- `12`: Start running the saved positions of the robotic arm.
- `14`: Reset the system and stop the running of saved positions.
- `16`: Move servo 1 in the positive direction.
- `17`: Move servo 1 in the negative direction.
- `18`: Move servo 2.
- `19`: Move servo 2.
- `20`: Move servo 3.
- `21`: Move servo 3.
- `22`: Move servo 4.
- `23`: Move servo 4.
- `24`: Move servo 5.
- `25`: Move servo 5.
- `26`: Move servo 6.
- `27`: Move servo 6.

Please note that additional commands and functionalities can be added to the code based on your specific requirements.

## Features

1. **Mecanum Wheels Control:** The vehicle can move in various directions - forward, backward, sideways, and rotate left or right, thanks to the Mecanum wheels.

2. **Bluetooth Remote Control:** You can control the vehicle using a Bluetooth-enabled device with a custom mobile app or any Bluetooth terminal application. The vehicle responds to commands sent via the Bluetooth module.

3. **Robotic Arm Movement:** The robotic arm can be controlled with the Bluetooth module to move its servos in both positive and negative directions. The arm's positions are stored in arrays for reusability.

4. **Speed Control:** The vehicle and the robotic arm's movements have adjustable speed through a custom slider control on the Bluetooth interface.

5. **Automatic Mode:** The vehicle can run pre-recorded steps to execute a sequence of movements, useful for repetitive tasks.

## Getting Started

1. **Hardware Setup:** Assemble the automation vehicle with Mecanum wheels and the robotic arm with hydraulic actuators. Connect the Arduino board and the servos as specified in the code.

2. **Upload the Code:** Upload the provided Arduino code to the Arduino board using the Arduino IDE.

3. **Bluetooth Connection:** Pair your Bluetooth-enabled device (e.g., smartphone or computer) with the HC-05 Bluetooth module. Use a Bluetooth terminal app or custom mobile app to send commands to the vehicle.

4. **Remote Control:** Use the following commands to control the vehicle:
   - '0': Stop moving
   - '1': Move forward
   - '2': Move backward
   - '3': Move right forward
   - '4': Move sideways left
   - '5': Move sideways right
   - '6': Move left backward
   - '7': Move right backward
   - '8': Rotate left
   - '9': Rotate right

5. **Controlling Robotic Arm:** Use commands '16' to '27' to control each servo of the robotic arm. The arm's speed can also be adjusted using a custom slider control (commands '101' to '150').

6. **Saving and Running Steps:** To save and run a sequence of steps, use the commands '12' and '14,' respectively.

## Notes

- The vehicle's battery voltage is monitored and indicated with an LED. If the voltage drops below 11V, the LED will turn on, indicating a low battery.

- The provided code serves as a basic framework for the robotic arm vehicle. Feel free to modify and extend the functionalities as per your specific requirements.

## Troubleshooting

If you encounter any issues or have questions about the project, feel free to raise an issue in this repository. We will be glad to assist you.

**Happy Building and Experimenting!**


### License

This project is licensed under the [MIT License](LICENSE).

Feel free to explore and modify the code according to your needs. Contributions and improvements are welcome!
