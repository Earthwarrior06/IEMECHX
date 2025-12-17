## Report: Important Observations on Ultrasonic and IR Sensors

### Aim

To study and simulate **distance sensing and obstacle detection** using **Ultrasonic (HC-SR04)** and **IR Obstacle Sensors**, and to observe their behavior, accuracy, and limitations.

---

## Theory

### Ultrasonic Sensor (HC-SR04)

The HC-SR04 works on the principle of **sound wave reflection** (SONAR). It emits ultrasonic sound waves (40 kHz) and measures the time taken for the echo to return after hitting an object.

**Distance Formula:**
[
Distance = rac{Time 	imes Speed\ of\ Sound}{2}
]

Where speed of sound ≈ 343 m/s.

---

## Observations

### Ultrasonic Sensor Observations

* Can measure **exact distance in centimeters**
* Works well for **transparent and opaque objects**
* Performance affected by **soft surfaces** (cloth absorbs sound)
* Accurate up to **2–300 cm range**
* Not affected by ambient light
* Slight delay due to time-of-flight calculation


## Comparison Table

| Feature                  | Ultrasonic Sensor | 
| ------------------------ | ----------------- | 
| Principle                | Sound reflection  | 
| Distance Measurement     | Yes (cm)          | 
| Range                    | 2–300 cm          |

---

## Simulation Results

* When an object was placed **within 20 cm**, LED and buzzer were activated
* For distances greater than 20 cm, outputs remained OFF
* Serial monitor displayed real-time distance values

---

## Applications

### Ultrasonic Sensor Applications

* Obstacle-avoiding robots
* Smart parking systems
* Distance measurement tools
* Water level monitoring


---

## Conclusion

Both sensors are effective for obstacle detection. The **ultrasonic sensor** is preferred when **accurate distance measurement** is required, while the **IR sensor** is suitable for **simple, low-cost, short-range detection**. The simulation successfully demonstrated obstacle detection using LED and buzzer alerts.

---
