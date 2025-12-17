## TASK 1 – Ultrasonic or IR Sensors (Week 1)

### Objective

Simulate an **obstacle-detection system** using an **HC-SR04 ultrasonic sensor** (or IR sensor alternative) that turns **LED + buzzer ON** when an object is closer than a threshold distance.

This submission includes:

* Arduino code
* Circuit diagram (text + pin map)
* Simulation steps (Tinkercad)
* GitHub repository structure

---

## Components (Simulation)

* Arduino Uno
* HC-SR04 Ultrasonic Sensor
* LED
* 220Ω resistor
* Buzzer
* Jumper wires

---

## Circuit Connections

### HC-SR04 → Arduino

| Sensor Pin | Arduino Pin |
| ---------- | ----------- |
| VCC        | 5V          |
| GND        | GND         |
| TRIG       | D9          |
| ECHO       | D10         |

### LED

* LED Anode → D6 (through 220Ω resistor)
* LED Cathode → GND

### Buzzer

* Buzzer + → D5
* Buzzer − → GND

---

## Arduino Code (Ultrasonic Obstacle Alert)

```cpp
// C++ code
//
long readUltrasonicDistance(int triggerPin, int echoPin)
{
  pinMode(triggerPin, OUTPUT);  // Clear the trigger
  digitalWrite(triggerPin, LOW);
  delayMicroseconds(2);
  // Sets the trigger pin to HIGH state for 10 microseconds
  digitalWrite(triggerPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(triggerPin, LOW);
  pinMode(echoPin, INPUT);
  // Reads the echo pin, and returns the sound wave travel time in microseconds
  return pulseIn(echoPin, HIGH);
}

void setup()
{
  pinMode(6, OUTPUT);
  pinMode(5, OUTPUT);
}

void loop()
{
  if (0.01723 * readUltrasonicDistance(9, 10) < 20) {
    digitalWrite(6, HIGH);
    digitalWrite(5, HIGH);
    delay(5); // Wait for 5 millisecond(s)
    digitalWrite(6, LOW);
    digitalWrite(5, LOW);
  }
}
```


