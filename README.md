# Obstacle Avoiding Robot using Arduino

This project is an Arduino-based robot that automatically detects and avoids obstacles using an ultrasonic sensor. It makes real-time decisions to change direction when an object is detected in its path.

## Features

- Detects obstacles using an HC-SR04 ultrasonic sensor
- Controls two DC motors to navigate and avoid obstacles
- Uses simple logic to move forward, stop, turn left or right
- Fully autonomous behavior

## Components Required

- Arduino Uno (or compatible board)
- HC-SR04 Ultrasonic Sensor
- L298N Motor Driver Module
- 2x DC Motors with wheels
- Chassis for robot
- Power supply (batteries)
- Jumper wires and breadboard (or soldered circuit)

## Wiring Overview

### Ultrasonic Sensor (HC-SR04)
| Pin  | Arduino Pin |
|------|--------------|
| VCC  | 5V           |
| GND  | GND          |
| Trig | D9           |
| Echo | D10          |

### Motor Driver (L298N)
| L298N Pin          | Arduino Pin / Power |
|--------------------|---------------------|
| IN1                | D2                  |
| IN2                | D3                  |
| IN3                | D4                  |
| IN4                | D5                  |
| ENA (enable A)     | Connected to 5V or PWM |
| ENB (enable B)     | Connected to 5V or PWM |
| VCC (motor power)  | Battery (e.g., 9V–12V) |
| GND                | GND                 |
| 5V (if onboard regulator present) | NC or Arduino 5V |

## Code Behavior

- Robot moves forward by default.
- If an obstacle is detected within a certain distance (e.g., 20 cm), the robot:
  - Stops
  - Turns either left or right
  - Continues moving forward once the path is clear

## Setup Instructions

1. Connect all components as described in the wiring table.
2. Upload the `Obstacle_Avoiding_Robot.ino` file to your Arduino board.
3. Power the robot using batteries.
4. Place the robot on the ground and observe it navigate around obstacles.

## Customization Tips

- Adjust the threshold distance (e.g., `20 cm`) in the code to change how soon it reacts.
- Add more sensors (like IR or side-mounted ultrasonic) for better navigation.
- Use PWM on ENA/ENB for speed control.

## License

This project is open-source and free to use under the MIT License.

## Credits

Created as a beginner-friendly autonomous robot project using Arduino and basic sensors.
