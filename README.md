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
Add the textures from ```fetch_gazebo/documents```.

Finally, edit the ```gazebo.material``` file found in ```/gazebo-$version/media/materials/scripts```. Add the following lines:
```bash
 material Gazebo/Image
    {
      technique
      {
        pass
        {
          ambient 0.5 0.5 0.5 1.0
          diffuse 1.0 1.0 1.0 1.0
          specular 0.0 0.0 0.0 1.0 0.5

          texture_unit
          {
            texture test1.png
            filtering trilinear
          }
        }
      }
    }

 material Gazebo/Image1
    {
      technique
      {
        pass
        {
          ambient 0.5 0.5 0.5 1.0
          diffuse 1.0 1.0 1.0 1.0
          specular 0.0 0.0 0.0 1.0 0.5

          texture_unit
          {
            texture test2.png
            filtering trilinear
          }
        }
      }
    }
 material Gazebo/Image2
    {
      technique
      {
        pass
        {
          ambient 0.5 0.5 0.5 1.0
          diffuse 1.0 1.0 1.0 1.0
          specular 0.0 0.0 0.0 1.0 0.5

          texture_unit
          {
            texture test3_big.png
            filtering trilinear
          }
        }
      }
    }
```
Everything should be working properly!

