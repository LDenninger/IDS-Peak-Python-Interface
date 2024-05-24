## IDS Peak Python Interface

Full python interface with usage of IDS Peak AFL and IPL host functions.
The repository includes a basic camera interface, a color corrector module and a manger for the auto features.

See `demo.ipynb` for basic usage.

SDK Manual:  https://en.ids-imaging.com/manuals/ids-peak/ids-peak-user-manual/2.8.0/en/index.html 


## Installation
### IDS Peak SDK
1. Download the debian package for the SDK from the peak website: https://en.ids-imaging.com/download-details/1009698.html?os=linux&version=&bus=64&floatcalc=
2. Install potential dependencies (not necessarily required):
```
 sudo apt-get install libqt5core5a libqt5gui5 libqt5widgets5 libqt5multimedia5 libqt5quick5 qml-module-qtquick-window2 qml-module-qtquick2 qtbase5-dev qtdeclarative5-dev qml-module-qtquick-dialogs qml-module-qtquick-controls qml-module-qtquick-layouts qml-module-qt-labs-settings qml-module-qt-labs-folderlistmodel libusb-1.0-0 libatomic1
```
3. Install IDS Peak: `sudo apt install ./ids-peak-with-ueyetl_2.8.0.0-16438_amd64.deb`
4. Increase USB buffer size to ensure proper bandwidth (not necessarily required):  `sudo /usr/local/scripts/ids_set_usb_mem_size.sh`

### Python Bindings
This installation guide is for a x86 system with Python 3.11. It might need to be adopted to your specific system

1. Install IDS Peak bindings: `pip install ids_peak-1.7.3.0-cp37-abi3-linux_x86_64.whl`
2. Install IDS Peak IPL bindings: `pip install ids_peak_ipl-1.11.0.0-cp310-cp310-linux_x86_64.whl`
3. Install IDS Peak AFL bindings: `pip install ids_peak_afl-1.4.0.0-cp37-abi3-linux_x86_64.whl`

## Troubleshoot

1. I had the problem that when installing IDS Peak 2.8.0, that the python bindings did not match the underlying IDS Peak version. I recommend using the newest version IDS Peak 2.9.0