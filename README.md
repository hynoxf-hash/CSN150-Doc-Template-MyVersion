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
