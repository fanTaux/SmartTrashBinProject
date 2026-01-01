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

- **Setup:** The hardware assembly involves connecting the ESP32 unit to the HC-SR04 ultrasonic sensor, DHT-11 temperature and humidity sensor, rain sensor, and a buzzer for audible alarms. Specific pin assignments must be followed, including GPIO 4 for the DHT11, GPIO 18 and 19 for the ultrasonic sensor, GPIO 39 for the rain sensor, and GPIO 23 for the buzzer. Following assembly, the source code containing Wi-Fi credentials, Thinger.io device information, and Telegram Bot tokens is uploaded to the ESP32 to establish connectivity via the MQTT protocol.
- **Demo:** The demonstration highlights the system's ability to provide real-time environmental monitoring by acquiring data from sensors every 20 seconds. It showcases the live visualization of water levels and humidity on the Thinger.io dashboard as well as the automated activation of the local buzzer and Telegram notifications. The alerting mechanism is demonstrated by simulating different water levels to trigger classification statuses: Waspada for 0-10 cm, Siaga for 10-20 cm, and Awas for levels exceeding 20 cm.
- **Evaluation:** The system is evaluated based on its accuracy in status classification and its response speed, or latency, when detecting water level changes. Testing results confirm the system's reliability in sending sequential notifications to residents (for example, at 18:00 and 18:02) during critical status transitions. This evaluation confirms the device's robustness in bridging information gaps during nighttime or extreme weather, effectively increasing evacuation response times compared to manual monitoring methods.

## Conclusion
This IoT-based flood early warning system can save lives, property, and effort for communities living in disaster-prone areas. Its automatic monitoring features, utilizing high-precision sensors such as the HC-SR04 and DHT-11, provide significant benefits by bridging the information gap between upstream river conditions and downstream residential settlements. With this system, we can foster a safer living environment integrated with future technology, ensuring that critical environmental data is accessible even during extreme weather or nighttime conditions. As long as this system is implemented and maintained effectively, we can advance disaster mitigation strategies with more accurate techniques and provide greater security for the public to focus on their daily activities without the constant threat of undetected rising water levels.

## Team
1. fanTaux (https://github.com/fanTaux)
2. cayo-py (https://github.com/cayo-py)
3. RisangDananJoyo (https://github.com/RisangDananJoyo)
