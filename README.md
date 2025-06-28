# Cyclone IV MIPI DSI 5.5-Inch LCD Interface Project

![Cyclone IV MIPI DSI LCD](https://img.shields.io/badge/Cyclone%20IV%20MIPI%20DSI%20LCD-Interface-blue)

## Overview

This repository contains the design files and code for interfacing a 5.5-inch LCD display using the Cyclone IV FPGA. The project leverages MIPI DSI technology for efficient data transmission and utilizes Verilog for hardware description.

## Table of Contents

- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- Supports MIPI DSI protocol for high-speed data transfer.
- Compatible with Cyclone IV FPGA from Intel (Altera).
- Implements LVDS to SLVS conversion for display communication.
- Easy integration with Quartus for FPGA programming.
- Verilog code provided for customization and extension.

## Hardware Requirements

To set up the project, you will need the following hardware components:

- Cyclone IV FPGA Development Board
- 5.5-inch TFT LCD Display with MIPI DSI interface
- Power supply for the FPGA board and display
- Jumper wires for connections
- Optional: Oscilloscope for signal testing

## Software Requirements

Ensure you have the following software installed:

- Intel Quartus Prime Software
- ModelSim for simulation (optional)
- Verilog simulator for testing the code

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/jhsdokfj/Cyclone-IV-MIPI-DSI-5.5-inch-LCD.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Cyclone-IV-MIPI-DSI-5.5-inch-LCD
   ```

3. Open the project in Intel Quartus.

4. Follow the setup instructions in the `docs` folder to configure your FPGA board.

5. Download the necessary files from the [Releases section](https://github.com/jhsdokfj/Cyclone-IV-MIPI-DSI-5.5-inch-LCD/releases) and execute them to program your FPGA.

## Usage

After installation, you can run the project by following these steps:

1. Connect the LCD display to the Cyclone IV FPGA board as per the wiring diagram in the `docs` folder.
2. Power on the FPGA board and the LCD display.
3. Load the Verilog design into Quartus and compile it.
4. Program the FPGA with the generated bitstream.
5. Use the provided example code to send data to the display.

### Example Code

Here is a simple example to display a pattern on the LCD:

```verilog
module lcd_display (
    input clk,
    input reset,
    output reg [23:0] pixel_data
);
    always @(posedge clk or posedge reset) begin
        if (reset) begin
            pixel_data <= 24'hFFFFFF; // White
        end else begin
            pixel_data <= 24'h000000; // Black
        end
    end
endmodule
```

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact

For questions or suggestions, please reach out:

- Email: example@example.com
- GitHub: [jhsdokfj](https://github.com/jhsdokfj)

For more information, visit the [Releases section](https://github.com/jhsdokfj/Cyclone-IV-MIPI-DSI-5.5-inch-LCD/releases) to download files and view updates.

## Topics

- Altera
- Cyclone IV
- FPGA
- Intel
- LCD Display
- LVDS to SLVS
- MIPI DPHY
- MIPI DSI
- Quartus
- TFT Display
- Verilog

![FPGA](https://img.shields.io/badge/FPGA-Development-orange)
![MIPI DSI](https://img.shields.io/badge/MIPI%20DSI-Protocol-green)
![LCD Display](https://img.shields.io/badge/LCD%20Display-Interface-red)

## Additional Resources

- [Intel Quartus Documentation](https://www.intel.com/content/www/us/en/programmable/support/support-resources.html)
- [MIPI Alliance](https://mipi.org/)
- [Verilog Language Reference](https://www.verilog.com/)

Feel free to explore the project and reach out if you need assistance. Your feedback is valuable for improving this repository.