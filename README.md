# 🎮 Arduino Labyrinth (Joystick Control)

## 📐 STL / CAD Files
👉 Contact: devranagiksu@gmail.com  

---

## 🎯 Description
This project is a **physical labyrinth controlled by a joystick**.  
Two servos tilt the platform so a ball can move through the maze.

- Joystick X/Y → Servo X/Y (platform tilt)  
- Ball → moves inside the maze  
- Neutral position → flat platform  

### Use cases
- 🎮 Game  
- 🏆 Competition / Olympiads project  
- 🎓 Engineering (SI) project  

---

## 🛠️ Hardware
- Arduino Uno  
- 2x Servo motors (SG90 or MG90S recommended)  
- 1x Analog joystick (A0, A1)  
- Breadboard + wires  
- 3D printed labyrinth  
- Ball (steel or plastic)  

---

## 📚 Libraries
- `Servo.h` (built-in)
- `Wire.h` (I2C LCD)
- `EEPROM.h` (sauvegarde calibration)


---

## 🔌 Wiring
| Component | Pin |
|----------|-----|
| Servo X  | 8   |
| Servo Y  | 9   |
| Joystick X | A0 |
| Joystick Y | A1 |
| VCC | 5V |
| GND | GND |

---

## 🚀 Installation
1. Connect all components  
2. Upload the Arduino code  
3. Power the circuit  
4. Adjust servo center positions if needed  

---

## 🎮 Controls
- Left / Right → Tilt X axis  
- Forward / Backward → Tilt Y axis  

---

## 🧠 Logic
- Reads joystick values (0–1023)  
- Converts to movement  
- Uses a deadzone to avoid noise  
- Limits servo angles for safety  

---

## ⚙️ Configuration
```cpp
int range = 12;        // Sensitivity
int threshold = 3;     // Deadzone
int ServoXHomePos = 103;
int ServoYHomePos = 134;
int maxTilt = 20;      // Max tilt
