# License Plate Recognition with OpenCV
This repo will help use your DepthAI device to find and take pictures of license plates on Linux
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

These curl/wget commands will vary based on your system
(venv) ~/license-plate-recognition-with-opencv $ bash -c "$(curl -fL http://docs.luxonis.com/_static/install_dependencies.sh)" # macOS
(venv) ~/license-plate-recognition-with-opencv $ sudo curl -fL http://docs.luxonis.com/_static/install_dependencies.sh | bash # 
(venv) ~/license-plate-recognition-with-opencv $ sudo wget -qO- http://docs.luxonis.com/_static/install_dependencies.sh | bash # Debian/Ubuntu
(venv) ~/license-plate-recognition-with-opencv $ python install_requirements.py
Installed
(venv) ~/license-plate-recognition-with-opencv $ sudo apt-get install libopencv-dev libtesseract-dev git cmake build-essential libleptonica-dev liblog4cplus-dev libcurl3-dev beanstalkd
Installed
(venv) ~/license-plate-recognition-with-opencv $ git clone https://github.com/openalpr/openalpr.git
Cloned repo
(venv) ~/license-plate-recognition-with-opencv $ cd openalpr/src
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ mkdir build
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ cd build
(venv) ~/license-plate-recognition-with-opencv/openalpr/src/build $ cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr -DCMAKE_INSTALL_SYSCONFDIR:PATH=/etc ..
(venv) ~/license-plate-recognition-with-opencv/openalpr/src/build $ make
(venv) ~/license-plate-recognition-with-opencv/openalpr/src/build $ sudo make install
Made install
(venv) ~/license-plate-recognition-with-opencv/openalpr/src $ cd ../../../
(venv) ~/license-plate-recognition-with-opencv $ sudo rm -r openalpr
(venv) ~/license-plate-recognition-with-opencv $ sh start.sh
Opens window
```
### How to use
After you run the last command in the installation section, a window should open with live footage of your DepthAI device.

The finding process wil start right after the script starts. After that, it will wait 3 seconds before starting again.
You can check if it found a license plate in the console
# Changelogs
### 0.0.2
Startup script called `start.sh`
### 0.0.1
Initial release
# Upcoming in 0.0.3
Installer.sh
# FAQs
### Can I run this on Windows?
Yes. With [Oracle VM VirtualBox](https://virtualbox.org) and the VirtualBox Extension pack, you can run Linux in a virtual machine and give the VM access to the USB port holding the DepthAI device. Just install a Linux distrubution of your choice in the VM and follow the steps in the installation section
### What do I do if I get an error `bash: git: command not found` or `bash: python: command not found` or `bash: apt: command not found`?
`bash: git: command not found` and `bash: python: command not found`: That means you need to install Git and Python via APT or your other package manager

`bash: apt: command not found`: Different Linux distros have different package managers. Debian, Ubuntu, and macOS use APT. Fedora, CentOS, and RedHat use Yum. Alpine Linux uses Pacman. openSUSE uses Zypper. To install the packages, run the APT commands above and replace `apt` with `yum` or `pacman` or `zypper`.
