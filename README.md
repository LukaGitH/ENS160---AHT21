# ENS160 + AHT21 Sensor Test (Arduino Uno)

This project reads and displays environmental data using the **ENS160 digital air quality sensor** and the **AHT21 temperature & humidity sensor**, both connected via I2C to an Arduino Uno.

## 🔧 Hardware Used

- **Arduino Uno**
- **ENS160** (Air Quality Sensor)
- **AHT21** (Temperature & Humidity Sensor)
- **I2C Wiring**

### 🧩 I2C Pin Connections (Arduino Uno)

| Arduino Uno | I2C Function | Sensor Pin |
|-------------|--------------|-------------|
| A4          | SDA          | SDA         |
| A5          | SCL          | SCL         |
| 5V          | VCC          | VCC         |
| GND         | GND          | GND         |

> ENS160 default I2C address used: `0x53`  
> AHT21 is auto-detected by the Adafruit library.

## 📦 Libraries Required

Install these libraries via the Arduino Library Manager:

- [`Adafruit AHTX0`](https://github.com/adafruit/Adafruit_AHTX0)
- `ScioSense_ENS160` (from Sciosense or GitHub)
- `Wire` (built-in)

## 🚀 How It Works

- Initializes both sensors.
- Reads temperature and humidity from the AHT21.
- Passes that data to the ENS160 to improve air quality readings.
- Prints **Temperature**, **Humidity**, **AQI**, **TVOC**, and **eCO2** to the Serial Monitor.
- Toggles the onboard LED every second.

## 🖥️ Serial Output Example

