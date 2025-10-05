🌱 Talking Plant Based on ESP32

📘 Project Overview
The Talking Plant System is an IoT-based smart plant monitoring system designed to help users understand and maintain their plant’s health.
Using an ESP32 microcontroller, the system continuously monitors temperature, humidity, soil moisture, and gas levels around a plant and provides real-time feedback through audio (speaker) and visual display (OLED) outputs.
This project aims to make plant care smarter and more interactive — allowing the plant to “talk” and express its needs.

⚙️ Components Used
Component	Description
ESP32	32-bit microcontroller with built-in Wi-Fi and Bluetooth. Acts as the brain of the project.
DHT11 Sensor	Measures temperature and humidity levels.
Soil Moisture Sensor	Detects water level in the soil to determine whether the plant needs watering.
MQ3 Gas Sensor	Detects gases and harmful fumes near the plant.
Relay Module (1-Channel)	Controls the water pump automatically when the soil becomes dry.
Speaker/Buzzer	Produces sound or voice responses from the plant.
OLED Display (128x64)	Displays live readings of sensors.
Power Supply (5V–9V)	Powers all components.

🧩 Working Principle
The ESP32 continuously reads data from the DHT11, MQ3, and Soil Moisture Sensor.
Sensor readings are compared against predefined threshold values.
If the soil moisture is low:
The relay activates the water pump automatically.
The speaker produces a voice alert like “I need water.”
If gas concentration is high:
The system alerts with a warning beep or message.
All parameters (temperature, humidity, soil moisture, gas level) are displayed on the OLED screen and printed in the Serial Monitor for debugging.
This allows the plant to "communicate" with the user — giving a sense of a “talking plant.”

🧠 Block Diagram Description
The block diagram represents the interconnection between sensors and the ESP32 controller:
Input Section: DHT11, MQ3, Soil Moisture Sensor
Processing Unit: ESP32
Output Section: OLED Display, Relay Module, Speaker
The ESP32 collects sensor data, processes it, and triggers the required output action.

⚡ Circuit Description
The circuit connects all components to the ESP32:
DHT11 Sensor → GPIO 27 (Digital)
MQ3 Gas Sensor → GPIO 34 (Analog)
Soil Moisture Sensor → GPIO 35 (Analog)
Relay Module → GPIO 25 (Digital)
Speaker/Buzzer → GPIO 26 (PWM)
OLED Display → I2C Pins (SDA, SCL)
Power Supply → 5V–9V DC input
Each sensor continuously sends data to the ESP32, which analyzes it and drives the outputs accordingly.
This simple and efficient setup makes the plant capable of self-monitoring and self-responding.

💻 Software Details
Platform: Arduino IDE
Libraries Used:
DHT.h (for DHT11 sensor)
Adafruit_SSD1306.h (for OLED display)
Wire.h (for I2C communication)
Programming Logic:
Initialize all sensors and pins in setup().
Continuously monitor environment variables in loop().
Compare values with threshold levels.
Trigger appropriate actions — display data, activate relay, or play alert sound.

🔍 Applications
Smart indoor plant care systems
Automated irrigation systems
Greenhouse environmental monitoring
Educational IoT demonstration projects

🚀 Future Scope
Add Wi-Fi connectivity for remote monitoring via a mobile app.
Integrate cloud data storage (Firebase, Blynk, or Thingspeak).
Include AI-based prediction models for plant health analytics.
Implement voice assistant integration (Alexa/Google Home).

🧾 License
This project is open-source under the MIT License.
You are free to use, modify, and distribute it for educational and non-commercial purposes.
