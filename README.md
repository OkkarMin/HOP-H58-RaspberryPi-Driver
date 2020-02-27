# HOP-H58 58mm Thermal Printer CUPS Driver for RaspberryPi

During my internship I was tasked with getting this [Hoin's HOP-H58 Thermal Printer](http://hoinprinter.com/en/products/show/58mm-Thermal-Printer-6) to work with RaspberryPi via USB connection. Linux drivers given on the offical Hoin website does not work with [CUPS](https://www.cups.org) on RaspberryPi. The reason being was that the offical drivers were compiled for 32bit whereas RaspberryPi was in 64bit.

Hence, I wrote a quick shell script to install correct dependencies and use the printer while plugged into RaspberryPi USB port

## Getting Started

### Prerequisites

- RaspberryPi with [Raspbian](https://www.raspberrypi.org/documentation/installation/installing-images/) installed
- CUPS
  - [Follow this guide](https://kernelmastery.com/enable-regular-users-to-add-printers-to-cups/) to ensure that you have proper permisison to interact with CUPS
- If possible, unplug any other external USB devices and only leave the printer USB plugged in

### Installing

1. Clone the repo
2. Make the install_H58_driver.sh executable
3. Run the script

```bash
cd HOP-H58-RaspberryPi-Driver
sudo chmod +x install_H58_driver.sh
./install_H58_driver.sh
```

## Authors

- [**Okkar Min**](https://github.com/OkkarMin)

## License

This project is licensed under the MIT License

## Acknowledgments

- [Adam James West](https://github.com/IntegersOfK) for his 64bit compiled filters for HOP-H58 drivers
