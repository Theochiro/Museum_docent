# Museum Docent

A Gazebo world where Fetch robot can explore and navigate freely.

## Installation

Make sure you have installed all fetch files for the [Gazebo Simulation](https://docs.fetchrobotics.com/gazebo.html).

Alternatively, run the following commands:
```bash
cd ~/catkin_ws/src
git clone https://github.com/Theochiro/Museum_docent
cd ..
catkin_make 
```
Next, edit the yaml file in ```fetch_gazebo/documents``` accordingly.

Now, we only need to modify the texture files in gazebo. First cd into the gazebo-$version:
```bash
cd /usr/share/gazebo-$version/media/materials/textures
```
Add the textures from using:
```bash
sudo mv ~/catkin_ws/src/Museum_docent/textures /usr/share/gazebo-$version/media/materials/textures/
```

Finally, replace the ```gazebo.material``` file found in ```/gazebo-$version/media/materials/scripts``` with the one provided:
```bash
 sudo mv ~/catkin_ws/src/Museum_docent/gazebo.material /usr/share/gazebo-$version/media/materials/scripts/
```
Everything should be working properly!

