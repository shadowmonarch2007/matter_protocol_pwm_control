# matter_pwm_control
ESP32-C6 Matter PWM Controller , To control the pwm of the gpio 
This project implements a Matter protocol smart device that provides three independent PWM-controlled dimmable lights. Each channel operates at 5kHz with 8-bit resolution (0-255), making it perfect for LED dimming applications. The device appears as three separate dimmable lights in your Matter ecosystem, allowing independent control of each channel through Google Home, Apple Home, or any Matter-compatible controller.
Built on the ESP32-C6 with ESP-Matter SDK, this controller demonstrates professional-grade Matter device development with clean architecture and robust PWM control.

Connect Hardware

1. Connect your ESP32-C6 board to your computer via USB
2. Identify the serial port (usually `/dev/ttyUSB0` on Linux or `/dev/ttyACM0`)
3. Connect your LEDs to GPIO 4, 5, and 6


Software Requirements

1. **ESP-IDF v5.0 or later**
   - Install from: https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/

2. **ESP-Matter SDK**
   - Install from: https://github.com/espressif/esp-matter

3. **Python 3.8+** (included with ESP-IDF)

4. **Git** (for cloning repositories)
5. ### Environment Setup

Make sure you have ESP-IDF and ESP-Matter properly installed and the environment variables set:

```bash
# Source ESP-IDF
. $HOME/esp/esp-idf/export.sh

# Source ESP-Matter
. $HOME/esp/esp-matter/export.sh
```
### Step 1: Clone or Navigate to Project

If this is a standalone project:
```bash
git clone <your-repo-url>
cd pwm_matter
```

If already in ESP-Matter examples directory:
```bash
cd $HOME/esp/esp-matter/examples/pwm_matter
```

### Step 2: Set Up Environment

```bash
# Load ESP-IDF tools and environment
. $HOME/esp/esp-idf/export.sh

# Load ESP-Matter environment
. $HOME/esp/esp-matter/export.sh
```

### Step 3: Configure the Project

```bash
# Set target to ESP32-C6
idf.py set-target esp32c6

# (Optional) Customize configuration
idf.py menuconfig
```

### Step 4: Build the Firmware

```bash
idf.py build
```
