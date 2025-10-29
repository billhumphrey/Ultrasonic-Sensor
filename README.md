
# Ultrasonic Distance Measurement with Arduino and LCD

This project demonstrates how to measure **distance using an ultrasonic sensor (HC-SR04)** connected to an **Arduino** and display the results on a **16x2 LCD via I2C communication**.
It’s a great beginner-friendly project to understand how ultrasonic sensors work for distance detection.


##  Components Required

| Component                   | Quantity | Description                      |
| --------------------------- | -------- | -------------------------------- |
| Arduino Board (Uno/Nano)    | 1        | Main microcontroller             |
| Ultrasonic Sensor (HC-SR04) | 1        | For measuring distance           |
| 16x2 LCD (with I2C Adapter) | 1        | For displaying distance readings |
| Jumper Wires                | —        | For circuit connections          |
| Breadboard                  | 1        | For assembling components        |

---

## 🔌 Circuit Connections

### **Ultrasonic Sensor (HC-SR04)**

| Sensor Pin | Arduino Pin |
| ---------- | ----------- |
| VCC        | 5V          |
| GND        | GND         |
| TRIG       | D5          |
| ECHO       | D6          |

### **I2C LCD Display**

| LCD Pin | Arduino Pin |
| ------- | ----------- |
| SDA     | A4          |
| SCL     | A5          |
| VCC     | 5V          |
| GND     | GND         |

---

##  How It Works

1. The **HC-SR04 sensor** emits an ultrasonic pulse through its **Trig pin**.
2. The pulse travels through the air, reflects off an object, and returns to the sensor.
3. The **Echo pin** receives the reflected pulse and measures the **time duration**.
4. Using the speed of sound, the Arduino calculates the **distance**.
5. The measured distance (in centimeters) is displayed on the **16x2 I2C LCD**.



##  Features

* Real-time **distance measurement**.
* **I2C LCD** for efficient display wiring.
* Simple and **low-cost** implementation.
* Great for projects like obstacle detection, parking sensors, or automation systems.

---

##  Troubleshooting

* **No reading on LCD:** Check I2C address (`0x27` or `0x3F`) — adjust in code.
* **Incorrect distance:** Ensure sensor faces a flat surface and avoid soft/absorbent materials.
* **No trigger response:** Verify TRIG and ECHO pin connections and 5V power supply.

