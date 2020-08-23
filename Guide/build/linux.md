# Linux Build Instructions for TIRTAGTXMRig-UPX

###
#### Navigate to your preffered folder first before cloning and building then open terminal and follow these commands : 
```
sudo apt-get update -y
sudo apt install git build-essential cmake libssl-dev libuv1-dev curl -y
sudo apt install libmicrohttpd-dev nano wget clang libclang-dev  htop -y
sudo apt update -y 
sudo apt upgrade -y
git clone https://github.com/TIRTAGT-DEV/TirtaXMRig-UPX.git
cd TirtaXMRig-UPX
cd build 
cmake .. 
make
./xmrig
```
