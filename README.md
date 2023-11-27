# quadruped-robot-ros2
HI~~~

ubuntu server 22.04

wifi setting

sudo cp /usr/share/doc/netplan/examples/wireless.yaml /etc/netplan 
sudo nano /etc/netplan/wireless.yaml 

https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html


mkdir puppypi_ws
cd puppy_ws
git clone https://github.com/BruceLin90620/quadruped-robot-ros2.git
colcon build --symlink-install
cd ~ 


pip3 install setuptools==58.2.0 

https://abyz.me.uk/rpi/pigpio/download.html
wget https://github.com/joan2937/pigpio/archive/master.zip
unzip master.zip
cd pigpio-master
make
sudo make install

sudo apt install ros-humble-joy
sudo apt install ros-humble-teleop-twist-joy

sudo su
ros2 launch puppy_bringup puppy_bringup.launch.py 

PermissionError: [Errno 13] Permission denied: '/dev/i2c-1'
sudo chmod 777 /dev/i2c-1

pip3 install smbus2

sudo pigpiod
sudo killall pigpiod
