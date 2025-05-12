# Google Assistant Controlled LEDs with Synric Pro & ESP32

This project demonstrates how to control LEDs using voice commands via Google Assistant, powered by an ESP32 microcontroller and Synric Pro.

---

## 📦 Components Required

- **Hardware:**
  - ESP32 Development Board
  - LED (e.g., WS2812 or standard RGB LED)
  - Resistors, jumper wires, and breadboard

- **Software:**
  - Arduino IDE
  - Synric Pro Library
  - Google Home App

---

## 🛠️ Installation Guide

### 1. Install Required Libraries:
   - Open Arduino IDE.
   - Go to **Sketch > Include Library > Manage Libraries**.
   - Search for and install the following libraries:
     - `SynricPro`
     - `Adafruit NeoPixel` (for WS2812 LEDs)
     - `ArduinoJson`
     - `WebSockets`

### 2. Set Up Synric Pro Account:
   - Visit [Synric Pro](https://sinric.pro/) and create a free account.
   - Add a new device (e.g., "LED Strip") and note down the **Device ID**, **App Key**, and **App Secret**.

### 3. Configure Arduino IDE:
   - Add ESP32 board support:
     - Go to **File > Preferences**.
     - In **Additional Boards Manager URLs**, add:
       ```
       https://dl.espressif.com/dl/package_esp32_index.json
       ```
     - Go to **Tools > Board > Boards Manager**, search for **ESP32**, and install it.

### 4. Upload Code to ESP32:
   - Open the example code from the Synric Pro library:
     - **File > Examples > SynricPro > RGB_LED_Stripe_5050**
   - Modify the code with your Wi-Fi credentials and Synric Pro credentials:
     ```cpp
     const char *ssid = "YOUR_SSID";
     const char *password = "YOUR_PASSWORD";
     const char *appKey = "YOUR_APP_KEY";
     const char *appSecret = "YOUR_APP_SECRET";
     const char *deviceId = "YOUR_DEVICE_ID";
     ```
   - Select the correct board and port:
     - **Tools > Board > ESP32 Dev Module**
     - **Tools > Port > COMx**
   - Upload the code to your ESP32.

---

## 📱 Google Home Integration

### 1. Link Synric Pro with Google Home:
   - Open the Google Home app.
   - Go to **Home > Add > Set up device > Works with Google**.
   - Search for and select **Synric Pro**.
   - Log in with your Synric Pro account.
   - Authorize Google Home to access your devices.

### 2. Control LEDs via Voice:
   - Use commands like:
     - “Hey Google, turn on the LED.”
     - “Hey Google, set the LED color to red.”
     - “Hey Google, set the LED brightness to 50%.”

---

## 🔧 Troubleshooting Tips

- **Device Not Responding:**
  - Ensure your ESP32 is connected to the internet.
  - Check the Serial Monitor for any error messages.

- **Incorrect Colors or Brightness:**
  - Verify your LED wiring and connections.
  - Ensure you're using the correct LED type in the code (e.g., `NEO_GRB + NEO_KHZ800` for WS2812).

- **Google Home Not Recognizing Device:**
  - Try unlinking and relinking the Synric Pro account in the Google Home app.
  - Ensure the device is properly configured in the Synric Pro dashboard.

---

## 📚 Additional Resources

- [Synric Pro GitHub Repository](https://github.com/sinricpro/esp8266-esp32-sdk)
- [Synric Pro Documentation](https://sinricpro.github.io/esp8266-esp32-sdk-documentation/index.html)
- [RGB LED Stripe Example Code](https://github.com/sinricpro/esp8266-esp32-sdk/blob/master/examples/Light/RGB_LED_Stripe_5050/RGB_LED_Stripe_5050.ino)

---

Feel free to modify this README to suit your project's specifics or to add more detailed instructions as needed.
