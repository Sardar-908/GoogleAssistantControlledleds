This project demonstrates how to control LEDs using voice commands via Google Assistant, powered by an ESP32 microcontroller and Synric Pro.

📦 Components Required
Hardware:

ESP32 Development Board

LED (e.g., WS2812 or standard RGB LED)

Resistors, jumper wires, and breadboard

Software:

Arduino IDE

Synric Pro Library

Google Home App
GitHub

🛠️ Installation Guide
Install Required Libraries:

Open Arduino IDE.

Navigate to Sketch > Include Library > Manage Libraries.

Search for and install:

SynricPro

Adafruit NeoPixel (for WS2812 LEDs)

ArduinoJson

WebSockets

Set Up Synric Pro Account:

Visit Synric Pro and create a free account.

Add a new device (e.g., "LED Strip") and note down the Device ID, App Key, and App Secret.
iotcircuithub.com
+1
Instructables
+1

Configure Arduino IDE:

Add ESP32 board support:

Go to File > Preferences.

In Additional Boards Manager URLs, add:

arduino
Copy
Edit
https://dl.espressif.com/dl/package_esp32_index.json
Go to Tools > Board > Boards Manager, search for ESP32, and install it.

Upload Code to ESP32:

Open the example code from the Synric Pro library:

File > Examples > SynricPro > RGB_LED_Stripe_5050

Modify the code with your Wi-Fi credentials and Synric Pro credentials:

cpp
Copy
Edit
const char *ssid = "YOUR_SSID";
const char *password = "YOUR_PASSWORD";
const char *appKey = "YOUR_APP_KEY";
const char *appSecret = "YOUR_APP_SECRET";
const char *deviceId = "YOUR_DEVICE_ID";
Select the correct board and port:

Tools > Board > ESP32 Dev Module

Tools > Port > COMx

Upload the code to your ESP32.

📱 Google Home Integration
Link Synric Pro with Google Home:

Open the Google Home app.

Go to Home > Add > Set up device > Works with Google.

Search for and select Synric Pro.

Log in with your Synric Pro account.

Authorize Google Home to access your devices.

Control LEDs via Voice:

Use commands like:

“Hey Google, turn on the LED.”

“Hey Google, set the LED color to red.”

“Hey Google, set the LED brightness to 50%.”

🔧 Troubleshooting Tips
Device Not Responding:

Ensure your ESP32 is connected to the internet.

Check the Serial Monitor for any error messages.

Incorrect Colors or Brightness:

Verify your LED wiring and connections.

Ensure you're using the correct LED type in the code (e.g., NEO_GRB + NEO_KHZ800 for WS2812).

Google Home Not Recognizing Device:

Try unlinking and relinking the Synric Pro account in the Google Home app.

Ensure the device is properly configured in the Synric Pro dashboard.
