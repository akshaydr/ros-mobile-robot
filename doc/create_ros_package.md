# Create basic ROS packages

We need to create following packages in the catkin workspace directory
 - mobile_robot
 - mobile_robot_base
 - mobile_robot_description
 - mobile_robot_simulation
 - mobile_robot_work

We will start assuming you dont have any project yet in ROS
## Step 1
Go to your catkin workspace
```bash
mkdir catkin_ws
cd ~/catkin_ws/
```
> *Note :* `cd` command is for changing the directory(change/goto a folder). `mkdir` command is for creating a new folder/directory, i.e. `catkin_ws`.

## Step 2
Initialize the workspace

```bash
mkdir src
cd src
catkin_init_workspace
```

## Step 3
Create packages

```bash
catkin_create_pkg mobile_robot_base rospy rviz geometry_msgs std_msgs sensor_msgs

catkin_create_pkg mobile_robot_description tf xacro urdf joint_state_publisher robot_state_publisher

catkin_create_pkg mobile_robot_simulation gazebo_ros
```

## Step 4
Create root package
```bash
catkin_create_pkg mobile_robot mobile_robot_base mobile_robot_description mobile_robot_simulation
```

## Step 5
Compile for the first time

go back to `catkin_ws` directory by running

```bash
cd ..
```

Now if you run `pwd` in the terminal, you should get an output like,
`/home/<USERNAME>/catkin_ws`

Here, run the following,
```bash
catkin_make

source devel/setup.bash
```
