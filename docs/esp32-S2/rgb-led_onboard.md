# How to Control the RGB LED on ESP32-S2-DevKitC-1

This guide explains how to control the built-in RGB LED on the ESP32-S2-DevKitC-1, connected to GPIO18.

---

## Prerequisites

1. Install **Arduino IDE**.
2. Install the **Adafruit NeoPixel** library:
   - Open Arduino IDE.
   - Go to **Tools > Manage Libraries**.
   - Search for and install **Adafruit NeoPixel**.
3. A USB cable to connect the board to your computer.

---

## Code to Control the RGB LED

Use this code to light up the LED and switch between red, green, and blue colors.

```cpp
#include <Adafruit_NeoPixel.h>

// RGB LED Configuration
#define LED_PIN 18         // GPIO18 connected to the RGB LED
#define NUM_PIXELS 1       // Only 1 built-in LED on ESP32-S2-DevKitC-1

// Initialize the NeoPixel object
Adafruit_NeoPixel strip(NUM_PIXELS, LED_PIN, NEO_GRB + NEO_KHZ800);

void setup() {
  strip.begin();           // Initialize the NeoPixel controller
  strip.show();            // Turn off all LEDs
}

void loop() {
  // Turn LED red
  strip.setPixelColor(0, strip.Color(255, 0, 0)); // Red
  strip.show();
  delay(1000);

  // Turn LED green
  strip.setPixelColor(0, strip.Color(0, 255, 0)); // Green
  strip.show();
  delay(1000);

  // Turn LED blue
  strip.setPixelColor(0, strip.Color(0, 0, 255)); // Blue
  strip.show();
  delay(1000);
}
```

---

## Uploading the Code

1. Connect your **ESP32-S2-DevKitC-1** to the computer via USB.
2. Configure the environment:
   - Go to **Tools > Board** and select **ESP32-S2 Dev Module**.
   - Set the correct port under **Tools > Port**.
3. Upload the code to the board.

---

## Additional Notes

- **If the LED doesn't light up:**
  - Ensure the RGB LED is connected to **GPIO18** (check the board's schematic).
  - Verify the **Adafruit NeoPixel** library is installed correctly.
  - Check for any physical damage on the board.

- **NeoPixel Protocol:** The RGB LED uses a specific protocol and won't work with simple `digitalWrite` commands.

- **Custom Colors:**
  - Change the values in `strip.Color(R, G, B)` to set different colors.

---

This guide provides a quick way to control the RGB LED on the ESP32-S2-DevKitC-1. Follow the steps carefully and test if the LED doesn’t work as expected.


