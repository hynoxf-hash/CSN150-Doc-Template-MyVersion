# Cybersecurity : CSN150  
## Project: ESP32-CAM Access Point (No Camera)

### Purpose
Set up the ESP32-CAM as a Wi-Fi access point and web server using the Arduino IDE, without connecting the camera module. Test that the ESP32 creates its own Wi-Fi network successfully.

### Equipment
- ESP32-CAM AI Thinker board (Aideepen W-BT with OV2640 support)  
- USB Type-C to Serial Port CH-340G cable  
- Computer with Arduino IDE installed  

### Links to Documentation and Tools
- [ESP32-CAM AP tutorial](https://randomnerdtutorials.com/esp32-cam-access-point-ap-web-server/)  
- [Arduino IDE](https://www.arduino.cc/en/software)  

### AI GPTs Used
- ChatGPT for code modification and troubleshooting  

### Steps I Followed
1. Installed ESP32 board support in Arduino IDE.  
2. Selected the **ESP32-CAM AI Thinker** board in the IDE.  
3. Opened the **CameraWebServer** example from Arduino IDE.  
4. Removed all code related to initializing and using the camera, since the camera was not connected.  
5. Replaced the Wi-Fi connection code (`WiFi.begin(...)`) with `WiFi.softAP(...)` to set up the ESP32 as an access point.  
6. Uploaded the modified sketch via USB without pressing the **BOOT** button.  
7. Opened the serial monitor to check if the ESP32 successfully created the access point.  
8. Connected my phone to the new Wi-Fi network (`ESP32-CAM-AP`) and verified the IP address (`192.168.4.1`).  

### Problems and Solutions
- **Problem:** The original code required the camera to be connected, or it would throw errors:  

------------------------------------------------------------------------------------------------




# ESP32-CAM Telegram Photo Project  
**YOUR_NAME : NOTES FOR CSN150**

## Purpose
The goal of this project is to set up an ESP32-CAM to take and send photos via Telegram, demonstrating IoT and Home Automation concepts learned in CSN150.

---

## Project Overview
- Create a Telegram bot to interact with ESP32-CAM.  
- Send `/photo` to the bot to have ESP32-CAM take a new photo.  
- Send `/flash` to toggle ESP32-CAM LED flash.  
- Send `/start` to get a welcome message with command instructions.  
- Only respond to messages from your Telegram account ID.

---

## Equipment Used
- ESP32-CAM board with OV2640 camera  
- USB cable  
- Computer  
- Internet access  

---

## Tools Used
- Arduino IDE  
- Telegram app (Android/iOS or PC)  
- Universal Arduino Telegram Bot Library  
- ArduinoJson Library  
---

## Steps I Followed
1. Installed Arduino IDE and ESP32 board support.  
2. Created a Telegram bot using BotFather and saved the bot token.  
3. Got my Telegram User ID using t.me/myidbot.  
4. Installed required libraries:  
   - Universal Telegram Bot Library (manually via .ZIP)  
   - ArduinoJson Library (v6.15.2)  
5. Copied example code to Arduino IDE and added:  
   - WiFi credentials (SSID and password)  
   - Telegram Bot token  
   - Telegram User ID  
6. Verified camera pinout for my ESP32-CAM board.  
7. Uploaded the sketch to the ESP32-CAM.  
8. Tested sending `/photo` to receive images via Telegram.  

---

## Problems / Solutions
- **Camera errors**  
  *Solution:* Checked camera module selection in Arduino IDE.  
- **Telegram bot not responding**  
  *Solution:* Ensured bot token and user ID were correctly added in the code.  
---

## Final Report
The ESP32-CAM was successfully set up to send photos via Telegram. All project steps, from bot creation to Arduino programming, were completed. Problems encountered were resolved by checking configurations and library versions.
---


## References
- [Random Nerd Tutorials: Telegram ESP32-CAM](https://randomnerdtutorials.com/telegram-esp32-cam-photo-arduino/)  
- [Universal Arduino Telegram Bot Library](https://github.com/witnessmenow/Universal-Arduino-Telegram-Bot)  
- [ArduinoJson Library](https://arduinojson.org/)

