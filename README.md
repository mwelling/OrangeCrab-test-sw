# OrangeCrab Test Software
This repository contains the software, firmware and gateware run on the OrangeCrab.

Software and gateware both utilise python, and the firmware is C

---
## Hardware ##
* OrangeCrab: [OrangeCrab Repo](https://github.com/gregdavill/OrangeCrab)
* OrangeCrab Test Fixture: [OranegCrab-test](https://github.com/mwelling/orangecrab-test)

## Usage ##

Current status: developing tests and workflow

To load the prebuilt firmware run the following steps
using `-S` loads the image directly into SRAM which is faster than FLASH, but not retained over a power cycle.
```
cd hw
ecpprog -S build/orangecrab/gateware/orangecrab.bit
```

You should see a device appear in `dmesg`
```
[369136.411380] usb 3-1.2: new full-speed USB device number 10 using xhci_hcd
[369136.560712] usb 3-1.2: New USB device found, idVendor=1209, idProduct=5bf2
[369136.560720] usb 3-1.2: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[369136.560726] usb 3-1.2: Product: OrangeCrab ACM
[369136.560733] usb 3-1.2: Manufacturer: GsD
[369136.562686] cdc_acm 3-1.2:1.0: ttyACM0: USB ACM device
````