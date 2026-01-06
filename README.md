# Smart Trashbin with Metal Detector and Range Sensor

<p align="center">
  <img src="assets/Skematik.jpeg" alt="Trashbin Project Banner" width="300">
</p>

## Project Domain
 <div align="justify"> This project presents a microcontroller-based solution designed for smart waste management in the Industry 5.0 era. It addresses the challenges of manual waste sorting, which is often time-consuming and results in low recycling rates. The system features an automated sorting mechanism that distinguishes metal from non-metal waste using electromagnetic induction. It also bridges the gap in waste monitoring by providing real-time bin capacity updates and automated notifications when the bin is full. By integrating sensors and actuators, this system ensures efficient waste segregation to support environmental sustainability. </div>


## Table Of Contents
- [Background](#background)
- [Prerequisites](#prerequisites)
- [System Diagrams](#system-diagrams)
- [Demo and Evaluation](#demo-and-evaluation)
- [Conclusion](#conclusion)
- [Team](#team)

---

## Background


### Problem Statements
1. Traditional waste management relies heavily on manual sorting, which is labor-intensive and time-consuming.
2. The inability to effectively separate metal from non-metal waste at the source complicates the recycling process and contributes to environmental pollution of soil, water, and air.
3. Without real-time monitoring, waste bins often overflow before being emptied, leading to unhygienic conditions and inefficient collection schedules.
4. There is a lack of immediate feedback or awareness for the public regarding the type of waste they are disposing of, which hinders long-term sustainability efforts.
   
### Goals
1. Develop a microcontroller-based system that can accurately detect and separate metal waste from non-metal waste automatically.
2. Implement a precise measurement system to track bin fullness and provide immediate visual status updates.
3. Provide clear audible and visual notifications to users and waste collectors when the bin reaches its maximum capacity.
4. Bridge the information gap in waste disposal by ensuring materials are sorted correctly at the point of entry to support broader recycling initiatives.

### Solution Statements
1. Utilize an Arduino Uno R3 as the primary processing unit to coordinate data from multiple sensors and manage actuator responses.
2. Incorporate an HC-SR04 ultrasonic sensor for precise capacity monitoring and an SN04 proximity sensor to identify metal objects through electromagnetic induction.
3. Employ an SG90 micro servo for automated lid control and an I2C LCD 16x2 to provide real-time visual feedback on bin status and waste types.
4. Integrate a physical buzzer to provide recurring audible alarms as a local notification when the waste capacity reaches 100%

---

## Prerequisites

### Hardware Specifications

- **Microcontroller:** ESP32 DEV KIT v4
- **Sensors:** Temperature Sensor (DHT-11), Ultrasonic Sensor (HC-SR04), & Rain Drop Sensor
- **Actuators:** Buzzer
- **Connectivity:** WiFi
- **Power Supply:** Direct USB Cable

### ESP32 Datasheet
<img src="assets/esp32v4pinout.png" alt="ESP32 Pinout" width="300">

### Thinger.Io Interface
<img src="assets/thinger.jpeg" alt="Blynk User Interface" width="300">

### Telegram Interface
<img src="assets/telegram.jpeg" alt="Blynk User Interface" width="300">

## System Diagrams

1.  **Block Diagram**

    ![Block Diagram](assets/blockdiagram.jpg)

2.  **Sequence Diagram**

    ![Sequence Diagram](assets/sequencediagram.jpg)

3.  **Flow Diagram**

    <img src="assets/FlowDiagram.png" alt="Flow Diagram" width="300">

4.  **Schematic**

    <img src="assets/Skematik.png" alt="Flow Diagram" width="300">


## Demo and Evaluation
### Demo Link : 

- **Setup:** The hardware assembly involves connecting an Arduino Uno R3 to an HC-SR04 ultrasonic sensor, SN04 proximity sensor, SG90 servo motor, 16x2 I2C LCD, and a buzzer. Specific pin assignments are followed according to the system schematic, utilizing digital pins for the ultrasonic sensor's trigger and echo, and the I2C protocol (SDA and SCL) for efficient display communication. Once the physical components are integrated on the breadboard, the source code containing the logic for capacity measurement, metal detection thresholds, and automated lid timing is uploaded to the Arduino to enable autonomous operation.
- **Demo:** The demonstration highlights the system's ability to provide real-time monitoring by acquiring sensor data and updating the I2C LCD status4444. It showcases the live visualization of waste capacity as a percentage and the classification of objects when they are detected within a 5cm range. The automated sorting is demonstrated when a metal object triggers the LCD to display "Sampah Logam Terdeteksi" and causes the servo to open the lid for 5 seconds6666. Furthermore, the local alert system is showcased by the buzzer sounding a recurring alarm every 1 minute once the capacity reaches 100%.
- **Evaluation:** The system is evaluated based on its accuracy in material classification and its response latency during object detection. Testing confirms the SN04 proximity sensor's reliability in identifying metal through electromagnetic induction and the HC-SR04 sensor's precision in tracking volume changes. Results indicate that the device effectively bridges the gap in waste management by providing immediate feedback to users, ensuring that materials are sorted correctly at the source. This evaluation confirms the robustness of the system in preventing bin overflow and increasing recycling efficiency compared to traditional manual sorting methods..

## Conclusion
<div align="justify"> The Smart Trash Bin project successfully demonstrates a microcontroller-based solution for automated waste management by integrating sensor technology with real-time feedback mechanisms. By utilizing an Arduino Uno to coordinate data from an HC-SR04 ultrasonic sensor and an SN04 proximity sensor, the system effectively automates the segregation of metal and non-metal waste while continuously monitoring bin capacity. The implementation of an automated servo-driven lid and a tiered alert system—featuring an I2C LCD and a physical buzzer—ensures timely disposal and prevents overflow by notifying users when the bin reaches 100% capacity. Ultimately, this project offers a scalable and efficient alternative to manual sorting, significantly improving recycling accuracy and supporting long-term environmental sustainability. </div>

## Team
1. Balevvvvy (https://github.com/Balevvvvy)
2. fanTaux (https://github.com/fanTaux)
3. RisangDananJoyo (https://github.com/RisangDananJoyo)
4. TaqiyudinMiftah (https://github.com/TaqiyudinMiftah)
