# 🚗 CAN Based Automotive Dashboard

An embedded systems project that implements a **CAN-Based Automotive Dashboard** using the **PIC18F4580** microcontroller. It receives real-time vehicle data over the **CAN protocol** and displays parameters such as speed, RPM, temperature, and fuel level on an LCD.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Challenges & Learnings](#challenges--learnings)
- [Future Enhancements](#future-enhancements)
- [Author](#author)

---

## 📖 Overview

This project simulates a real-time **automotive dashboard** built around the PIC18F4580 microcontroller. Vehicle parameters transmitted over the **CAN (Controller Area Network)** bus are received, decoded, and displayed on an LCD in real time. The firmware is developed in **Embedded C using MPLAB IDE**, and firmware updates are handled via **Tiny Bootloader**, eliminating the need for an external programmer.

---

## ✨ Features

- 📡 **CAN Communication** — Receives real-time vehicle data over the CAN protocol
- 🖥️ **Real-Time Display** — Shows speed, RPM, temperature, and fuel level on an LCD
- 🔄 **Bootloader Support** — Firmware updates via Tiny Bootloader over UART, without an external programmer
- ⚙️ **Multi-Peripheral Integration** — Combines CAN module, LCD, and UART for reliable operation
- 🚘 **Automotive Application** — Simulates real-world vehicle dashboard behavior

---

## 🛠️ Technologies Used

- **Microcontroller:** PIC18F4580
- **Language:** Embedded C
- **IDE:** MPLAB
- **Bootloader:** Tiny Bootloader
- **Protocol:** CAN (Controller Area Network)
- **Display:** Character LCD

---

## 📂 Project Structure

```
CAN-Automotive-Dashboard/
├── src/
│   ├── main.c
│   ├── can_config.c
│   ├── lcd_driver.c
│   └── dashboard.h
├── bootloader/
│   └── TinyBootloader/
├── docs/
│   └── circuit_diagram.png
└── README.md
```

> Note: Update this structure to match your actual repository layout.

---

## 🚀 Getting Started

### Prerequisites
- MPLAB IDE installed
- PIC18F4580 microcontroller (or compatible development board)
- Tiny Bootloader software
- CAN transceiver module and CAN bus setup
- Character LCD display

### Installation & Flashing

```bash
# 1. Open the project in MPLAB IDE
# 2. Build the project to generate the .hex file
# 3. Connect the PIC18F4580 board via UART
# 4. Open Tiny Bootloader and select the correct COM port
# 5. Load the generated .hex file and flash the firmware
```

---

## 💻 Usage

1. Power on the PIC18F4580 board connected to the CAN bus network.
2. The microcontroller continuously listens for incoming CAN messages from other nodes on the network.
3. Received messages are decoded and relevant parameters are extracted.
4. The LCD updates in real time to display:
   - Speed
   - RPM
   - Temperature
   - Fuel Level

---

## ⚙️ How It Works

1. **CAN Message Reception**
   - The CAN module on the PIC18F4580 is configured to receive messages from connected CAN nodes.
2. **Data Decoding**
   - Incoming CAN messages are parsed to extract individual vehicle parameters.
3. **LCD Update**
   - Decoded values are formatted and displayed on the character LCD with minimal delay.
4. **Firmware Updates**
   - New firmware can be uploaded via Tiny Bootloader over UART, without needing an external hardware programmer.

---

## 🧩 Challenges & Learnings

- **CAN Communication Setup:** Overcame message configuration and synchronization issues by properly configuring the CAN module and verifying transmission/reception.
- **Real-Time Data Display:** Achieved efficient data processing by decoding CAN messages correctly and updating the LCD with minimal delay.
- **Bootloader Programming:** Configured the serial interface correctly to enable firmware uploads via Tiny Bootloader without an external programmer.
- **Multi-Peripheral Integration:** Strengthened understanding of embedded C, CAN protocol, and microcontroller architecture by reliably integrating the CAN module, LCD, and UART together.

---

## 🔮 Future Enhancements

- Add support for additional vehicle parameters (battery voltage, tire pressure, etc.)
- Implement a graphical display (TFT/OLED) instead of character LCD
- Add data logging for diagnostic purposes
- Integrate wireless telemetry (Bluetooth/Wi-Fi) for remote monitoring

---

## 👤 Author

**S Vibin Michael**
- 📧 Email: [vibinmichael18@gmail.com](mailto:vibinmichael18@gmail.com)
- 💼 LinkedIn: [vibin-michael](https://www.linkedin.com/in/vibin-michael-46b4b7316)
- 🐙 GitHub: [vibinmichael18-qq](https://github.com/vibinmichael18-qq)

---

<p align="center"><i>⭐ If you found this project useful, consider giving it a star!</i></p>
