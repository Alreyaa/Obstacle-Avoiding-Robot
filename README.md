# 🤖 Obstacle Avoiding Robot with Servo using Arduino

An autonomous robot that navigates its environment while avoiding obstacles using an **ultrasonic sensor mounted on a servo motor**, an **Arduino Uno**, and a **motor driver**. The servo rotates the ultrasonic sensor to scan left and right, giving the robot a better idea of where to go.

## 🧠 Gist of the Project

This project demonstrates the basics of robotics and sensor integration. Using a combination of **ultrasonic distance sensing**, **servo-controlled scanning**, and **DC motor control**, the robot continuously scans for obstacles and avoids collisions by changing direction. This dynamic system mimics real-world autonomous navigation at a basic level.

## 📦 Prerequisites

Make sure you have the following software and libraries installed:

- **Arduino IDE** 
- **NewPing Library** – Required for interfacing with the HC-SR04 ultrasonic sensor

### 🛠️ Installing the NewPing Library

1. Open the Arduino IDE.
2. Go to **Sketch > Include Library > Manage Libraries...**
3. In the Library Manager, search for **"NewPing"**.
4. Click **Install** on the **NewPing** library by Tim Eckel.

## 🧰 Components Required

| Component                   | Quantity |
|-----------------------------|----------|
| Arduino Uno                 | 1        |
| HC-SR04 Ultrasonic Sensor   | 1        |
| Mini Servo Motor (SG90)     | 1        |
| L298N Motor Driver Module   | 1        |
| DC Motors with Wheels       | 2        |
| Robot Chassis Kit           | 1        |
| Breadboard                  | 1        |
| Jumper Wires                | Several  |
| 9V Battery + Connector      | 2        |
| Caster Wheel                | 1        |

## ⚙️ Connections

### ⚫ Breadboard Connections

- Use the breadboard to split 5V and GND to both the **ultrasonic sensor** and the **servo motor**.
- Connect **Arduino 5V** to the breadboard’s **+ rail**.
- Connect **Arduino GND** to the breadboard’s **– rail**.

### 🟦 HC-SR04 Ultrasonic Sensor → Arduino

| HC-SR04 Pin | Arduino Pin    |
|-------------|----------------|
| VCC         | 5V(breadboard) |
| GND         | GND            |
| Trig        | Digital pin 9  |
| Echo        | Digital pin 10 |

### 🔄 SG90 Servo Motor → Arduino

| Servo Wire      | Arduino Pin     |
|-----------------|-----------------|
| VCC (Red)       | 5V (breadboard) |
| GND (Brown)     | GND (breadboard)|
| Signal (Orange) | D11 |

### ⚡ L298N Motor Driver → Arduino & Motors

| L298N Pin   | Arduino Pin    |
|-------------|----------------|
| IN1         | Digital pin 7  |
| IN2         | Digital pin 6  |
| IN3         | Digital pin 5  |
| IN4         | Digital pin 4  |
| OUT1 & OUT2 | DC Motor 1     |
| OUT3 & OUT4 | DC Motor 2     |
| VCC         | 9V Battery     |
| GND         | Common Ground  |
| 5V          | Vin            |

## 🚀 Uploading the Code

1. Install the **NewPing** library if not already installed (see above).
2. Open Arduino IDE.
3. Connect the Arduino Uno to your PC using USB.
4. Open the `.ino` file containing your obstacle avoiding robot code.
5. Go to **Tools > Board > Arduino Uno**.
6. Select the correct **COM Port** under **Tools > Port**.
7. Click the **Upload** button.
8. Once uploaded, disconnect USB and connect the 9V battery to power the robot.

## 🧪 Testing

- Place the robot on a flat surface.
- After uploading the code and powering it, the robot will:
  - Rotate the ultrasonic sensor using the servo
  - Scan left, center, and right
  - Move forward if the path is clear
  - Change direction based on obstacle position

## 🧾 Reference

- Instructables Guide: [Obstacle Avoiding Robot](https://www.instructables.com/Obstacle-Avoiding-Robot-Arduino-1/)

## 📄 License

This project is licensed under the MIT License.
