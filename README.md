# Data Transmission Using Low-Cost Li-Fi

A MATLAB-based implementation of image transmission over Li-Fi using low-cost hardware via serial communication.

---

## Table of Contents

- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Authors and Contributors](#authors-and-contributors)

---

## About the Project

This project implements a Li-Fi (Light Fidelity) based data transmission system using MATLAB and low-cost hardware components. It demonstrates how image data can be transmitted wirelessly through light signals by encoding pixel values and sending them serially over a COM port, simulating the core principle of Li-Fi communication at a hardware level.

The project addresses the high cost and complexity typically associated with Li-Fi research by building a working proof-of-concept using affordable components and MATLAB's serial communication capabilities. It consists of two separate scripts — a transmitter that reads, resizes, and serially sends an image, and a receiver that reconstructs it — making it accessible for academic research and experimentation.

---

## Key Features

- **Image Transmission over Li-Fi:** Reads a real image, converts it to grayscale, resizes it to 10×10, and transmits each pixel value serially to simulate Li-Fi data transfer.
- **Serial Communication:** Uses MATLAB's serial interface to send and receive data over a COM port at a configurable baud rate.
- **Transmitter and Receiver Architecture:** Separate transmitter and receiver scripts that mirror a real-world Li-Fi communication system end to end.
- **Low-Cost Hardware Focus:** Designed to work with affordable components, making Li-Fi experimentation accessible without specialized equipment.

---

## Tech Stack

| Layer    | Technology                        |
|----------|-----------------------------------|
| Language | MATLAB                            |

---

## Installation

### Prerequisites

- MATLAB with Image Processing Toolbox — verify by running `ver` in the MATLAB command window
- A serial COM port connection with compatible hardware

### Steps

1. Clone the repository
```bash
   git clone https://github.com/Bharath2228/The-Data-Transmission-Technique-Using-Low-Cost-Li-Fi.git
   cd The-Data-Transmission-Technique-Using-Low-Cost-Li-Fi
```

2. Open MATLAB and navigate to the project folder
```matlab
   cd('path/to/The-Data-Transmission-Technique-Using-Low-Cost-Li-Fi')
```

---

## Usage

### Running the Project

Run the receiver script first on the receiving end, then run the transmitter:
```matlab
% Step 1 — run on the receiver side
run('Main_Reciever.m')

% Step 2 — run on the transmitter side
run('Main_transmitter.m')
```

Before running, open both `Main_transmitter.m` and `Main_Reciever.m` and update the COM port to match your hardware:
```matlab
s = serial('COM9');  % Change COM9 to your actual port
```

### Input Files

| File / Parameter | Description                                              | Where to Get It      |
|------------------|----------------------------------------------------------|----------------------|
| `dsa.jpg`        | Sample image used as the transmission payload            | Already in the repo  |

### Output

| Output          | Description                                                        | Location        |
|-----------------|--------------------------------------------------------------------|-----------------|
| Reconstructed image | The received 10×10 grayscale image displayed in a MATLAB figure | MATLAB figure window |
| Terminal output | Pixel values printed to the MATLAB command window during transfer  | MATLAB console  |

---

## Project Structure
```
The-Data-Transmission-Technique-Using-Low-Cost-Li-Fi/
├── Main_transmitter.m   # Reads, processes, and transmits image data over serial
├── Main_Reciever.m      # Receives serial data and reconstructs the image
├── recieverLIFI.m       # Supporting receiver logic
├── test.m               # Test script for verifying serial communication
└── dsa.jpg              # Sample image used as the transmission payload
```

---

## Authors and Contributors

**Bharath** — [@Bharath2228](https://github.com/Bharath2228)
