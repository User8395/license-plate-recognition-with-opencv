# License Plate Recognition with OpenCV
This repo will help use your DepthAI device to find and take pictures of license plates
### Installation
Run these commands (the text after the $'s) in order
```
~ $ git clone https://github.com/qaqak/license-plate-recognition-with-opencv.git
Cloned repo
~ $ cd license-plate-recognition-with-opencv
~/license-plate-recognition-with-opencv $ sudo apt install python3-venv
[sudo] password for user: 
Installed
~/license-plate-recognition-with-opencv $ python3 -m venv venv
~/license-plate-recognition-with-opencv $ source venv/bin/activate
(venv) ~/license-plate-recognition-with-opencv $ python install_requirements.py
Installed
(venv) ~/license-plate-recognition-with-opencv $ sudo apt-get install libopencv-dev libtesseract-dev git cmake build-essential libleptonica-dev
Installed
(venv) ~/license-plate-recognition-with-opencv $ sudo apt-get install liblog4cplus-dev libcurl3-dev
Installed
(venv) ~/license-plate-recognition-with-opencv $ sudo apt-get install beanstalkd
Installed
(venv) ~/license-plate-recognition-with-opencv $ git clone https://github.com/openalpr/openalpr.git
Cloned repo
(venv) ~/license-plate-recognition-with-opencv $ cd openalpr/src
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ mkdir build
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ cd build
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr -DCMAKE_INSTALL_SYSCONFDIR:PATH=/etc ..
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ make
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ sudo make install
Made install
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ cd ../../
(venv) ~/license-plate-recognition-with-opencv $ sudo rm -r openalpr
(venv) ~/license-plate-recognition-with-opencv $ python3 depthai_demo.py -cnn vehicle-license-plate-detection-barrier-0106 -s previewout metaout jpegout
Opens window
```
### How to use
After you run the last command in the installation section, a window should open with live footage of your DepthAI device.

Press the `c` key on your keyboard to begin the finding process
# Changelogs
### 0.0.1
Initial release
# Upcoming in 0.0.2
Startup script called `start.sh`
