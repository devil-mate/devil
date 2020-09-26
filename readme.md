[toc]
# 总体框架
说明：
myrobot_proj作为功能包集，下面包括各个功能包：
mygazebo: 启动gazebo仿真环境（加载world和robot）;包括了world模型，要能加载自己的机器人和其他ros机器人。
ros_robot包： 存放多种机器人文件，包括ros下载的机器人（自己写的urdf模型在mygazebo中），用于mygazebo加载。{或者应该把world模型放在这里来}
myrobot_simulator: 只是个文件夹，用作文件组织结构，包括各种仿真包（和这个平级的可以是用在实际机器人上的代码）
	仿真功能：激光slam、vslam、导航功能;
	另外加一些辅助功能：如按键控制包、gui、以及gazebo插件（应该放在mygazebo包里面）
# 
1.利用已有模块，快速搭建demo，实现turtlebot的定位与导航仿真，
2. 直接利用turtlebot_description包，启动turtlebot机器人模型。
myrobot_proj 的文件组织结构：
	a.myrobot_gazebo  在gazebo启动一个机器人模型，可以是自己的模型，如mygazebo包中的小车，也可以是turtlebot或其他git上的模型。所以，都是已有的模型，这个包里只需要启动文件，或者再加一些worlds，或者把自己建立的机器人模型和world可以都放在一起，不用到处找，只需要再launch中改变机器人名字就可以了，比如mygazebo中，或者就像turtlebot一样，做一个turtlebot_description包。
	b.navigation功能包集合的使用http://wiki.ros.org/cn/navigation/Tutorials/RobotSetup,也是一些launch文件及配置文件，因为源程序已有包。



myobot_simulator： 利用已有的源程序/包搭建应用。
myrobot_apps: 自己实现各种包，slam，navigation
	
	

