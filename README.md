# SD.NEXT-ANDROID-TERMUX-
Wooooooooohhhhhhhhooooo you can install SD.NEXT on Android!¡!


DISABLE PHANTOM PROCESS KILLLER OR U WON'T BE ABLE TO MAKE IMAGES OVER 320X320!!!!


You need at least 8-12-16 gb ram device to use this I'm still trying to figure out y triton won't install,if someone figures it out please let me know. but sdxl models do load on sdnext but no images will generate. I think it's because triton  won't install. plz someone figure it out cuz I can't 🙏 


1. Prerequisites
First you have to install Termux and install PRoot. Then install and login to Ubuntu in PRoot



pkg updated && pkg upgrade -y && termux-setup-storage &&
pkg install wget -y && pkg install git -y && pkg install proot -y &&
cd ~ && git clone https://github.com/MFDGaming/ubuntu-in-termux.git && cd ubuntu-in-termux && chmod +x ubuntu.sh && ./ubuntu.sh -y && ./startubuntu.sh 


2. Installing SD.NEXT
Run below commands sequentially as root user in Ubuntu

Install basic tools

apt update && apt upgrade -y && apt-get install curl git gcc make build-essential python3 python3-dev python3-distutils python3-pip python3-venv python-is-python3 -y 

Install required extensions

apt-get install libgl1 libglib2.0-0 libsm6 libxrender1 libxext6 -y

Clone the repository

git clone https://github.com/vladmandic/automatic.git


Change the current directory

cd automatic 


'Fix' the issue with Python running in PRoot

export ANDROID_DATA=anything 

Install required Python packages

pip install -r requirements.txt

Install xformers. This package is not required, but is recommended to be installed
pip install xformers 

Launch the webui. It will take some time to complete first-time installation then everything should be fine

python launch.py --use-cpu all --lowvram



Navigate to the webui in your browser
http://127.0.0.1:7860 

To start after rebooting termux after first installation 

THEN PASTE BOTTOM COMMAND 

cd ubuntu-in-termux && ./startubuntu.sh

cd automatic && python launch.py --use-cpu all --lowvram
