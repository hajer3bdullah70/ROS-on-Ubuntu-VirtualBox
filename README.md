# ROS-on-Ubuntu-VirtualBox

### 1. Installing VirtualBox

Download it from  website by [click here.](https://www.virtualbox.org/wiki/Downloads)

now after downloading VirtualBox you can download and run any OS you like through it

### 2. Downloading Ubuntu
Download it from  website by [click here.](https://ubuntu.com/download)

### 3. Creating a new Virtual Machine

now open VirtualBox then Click "New" Button

![image](https://user-images.githubusercontent.com/107868812/179498906-238e9e38-1199-4e4e-9b55-f799fe2454d2.png)

and it's gonna ask us for a name so we are going to name it "Ubuntu20.04" or whatever version you have downloaded.
the type we are going to select "Linux" and the version Ubuntu(64-bit)

![image](https://user-images.githubusercontent.com/107868812/179499067-bbfb781c-b889-46f8-8d8a-b68227e7ed84.png)

for memory size you need at least 4GB RAM

![image](https://user-images.githubusercontent.com/107868812/179499167-7cc6912a-236e-4c17-b7f3-6a63916c6ea7.png)


The next three things we are going to leave it as default

![image](https://user-images.githubusercontent.com/107868812/179499228-386e0925-f6d5-4945-aedc-ccb86c421408.png)

![image](https://user-images.githubusercontent.com/107868812/179499248-c6d4d954-7f0c-4f52-970f-d09920c49235.png)

![image](https://user-images.githubusercontent.com/107868812/179499277-bd319dfe-9dfe-471a-a9a5-1cb8bfc30228.png)

for the disk space at least give it a 25GB

![image](https://user-images.githubusercontent.com/107868812/179499714-c5219c0f-dbec-4cca-96ad-89a0e5465ed8.png)


### 4. Modify in the settings

now we have created the Virtual Machine so now we have to modify a few things in the settings click on Ubuntu then on the settings.

![image](https://user-images.githubusercontent.com/107868812/179499840-75a3130e-6fdc-41f9-8bd8-ee2f43b3da00.png)


now go to Advanced and make sure those two options are "Bidirectional" so you can be able to copy and paste in and out of it

![image](https://user-images.githubusercontent.com/107868812/179499902-cfef5ed1-7325-41e1-adf4-f7b75251e993.png)


next is "System" i'll show you my settings and i recommend the same (you can max it all through the green area)

![image](https://user-images.githubusercontent.com/107868812/179499959-5c07f63c-6957-4549-9bd3-3370f8b96eef.png)


in CPU the minimum is 2

![image](https://user-images.githubusercontent.com/107868812/179500025-74f09d01-5516-4d30-8b92-c39fe789bca6.png)


now in "Display" i'm going to max "Video memory" as well but the default is fine also.

![image](https://user-images.githubusercontent.com/107868812/179500089-9841df9f-33c7-4d42-84db-8a668d927590.png)

now the important part here in the "storage" i'm going to select the empty disk then click on the CD on the right and click on "Choose a disk file" from here we are going to select the ubuntu Image file that we have downloaded

![image](https://user-images.githubusercontent.com/107868812/179500153-ce595607-cb0a-4f78-9308-6529508141f6.png)

and the rest of the settings i'm going to leave it as default

now we are going to select the installation then click on "Start" in the start-up disk make sure to select the "ubuntu iso image disk" then click start

![image](https://user-images.githubusercontent.com/107868812/179500209-b4004443-05f8-4817-a82b-bba9da21172f.png)

next you can select your language then press "Install Ubuntu"

![image](https://user-images.githubusercontent.com/107868812/179500294-de5bc0ee-b643-47fb-b93b-6bb6a03980a4.png)

![image](https://user-images.githubusercontent.com/107868812/179500312-ccc69f8f-fef7-4764-8c93-bc1b273757bf.png)

![image](https://user-images.githubusercontent.com/107868812/179500332-6cb33e46-7dba-4d5b-a242-ae4f529cbff2.png)

Write your name or your computer's name, for username you can change it as you like and set a password and make sure you remember it because you are going to use it a lot as a permission key on Ubuntu.


![image](https://user-images.githubusercontent.com/107868812/179500386-90cf7c79-5cfd-4143-a551-a4e1ff4289f2.png)

now after the restart we are almost done and we got this desktop but it's a small box, we are going to write a few commands so it fit in the screen like a normal desktop, open the menu and search for "Terminal" from here

![image](https://user-images.githubusercontent.com/107868812/179500437-b96c87c0-018c-4a55-85c5-239917ce3d23.png)

now in the terminal we will run an update command

     sudo apt-get update

it's going to ask for your password that you have assigned.
now run the upgrade command

     sudo apt-get upgrade
     
now the last command

     sudo apt install build-essential dkms linux-headers-$(uname -r)
     
write "Y" if it asked to allow to continue the operation
after finished close the terminal then go to the "Devices" in the menu at the top and select "Insert Guest Additions CD image..."

![image](https://user-images.githubusercontent.com/107868812/179501035-02a85d5a-9791-4e7a-bfc6-ceb1cf0d3f02.png)

click on "Run" then type your password then click on "Authenticate" a window will show up and asks you to press "Enter" to close the window then restart your system.


![image](https://user-images.githubusercontent.com/107868812/179501202-0083f5e1-d1c5-42c8-9515-fa2a3d66c81b.png)

after restarting you won't notice anything diffrent until you minimize Ubuntu window then maximize it again then it will fit in your screen, and if you just go to "View" menu and select "Full screen Mode" it will take over the entire screen.

![image](https://user-images.githubusercontent.com/107868812/179501301-b4120737-dada-467d-9793-286e3f3096de.png)

### 4. Install of ROS neotic
this is the last and easiest step for now you just have to open the terminal again and copy and paste these commands.
Setup your computer to accept software from packages.ros.org by using this command

    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    
Set up your keys

    sudo apt install curl

    curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
   
updating

    sudo apt-get update


ROS distributions are linked to Ubuntu versions:

- Ubuntu 20.04 -> Noetic
- Ubuntu 18.04 -> Melodic
- Ubuntu 16.04 -> Kinetic

now i'm using Ubuntu 20.04 so i'll install neotic, you can change "neotic" to one of the above depending on what version you are working with!
Installing ROS neotic Desktop-Full ,Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages

    sudo apt-get install ros-noetic-desktop-full

Environment setup

    echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
    
    source ~/.bashrc
    
    sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
    
    sudo apt install python3-rosdep
   
    sudo rosdep init
    
    rosdep update
    
    mkdir -p ~/catkin_ws/src
    
    cd ~/catkin_ws/
    
    catkin_make
    
    cd ~/catkin_ws/src

here you can clone any project you want from Github, i will use the Arduino robot arm from Smart-Methods

    git clone https://github.com/smart-methods/arduino_robot_arm.git 
    
    cd ~/catkin_ws
    
    rosdep install --from-paths src --ignore-src -r -y
    
    sudo apt-get install ros-noetic-moveit
    
    sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
    
    sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
    
    sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
    
    catkin_make
    
Launching ROS on a project from @Smart_methods for a robotic arm

    roslaunch robot_arm_pkg check_motors.launch

### Finally!
![image](https://user-images.githubusercontent.com/107868812/179503567-278706c6-482b-468d-96fd-42965c37c184.png)



    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    




