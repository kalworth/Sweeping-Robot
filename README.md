### 功能包说明
- **robot** 包含扫地机器人的.urdf文件和环境的.world文件
- **m-explore** 开源的explore_lite算法
- **manual_nav** 手动建图和手动导航的功能包
- **auto_nav** 自主建图和自主导航的功能包
    - *path_planning.cpp* 为扫地路径规划代码
    - *path_planning_node.cpp* 发布规划好的路径的节点
    - *next_goal.cpp* 发布下一个目标点的节点

### 使用说明
1. 在该工程的根目录编译项目： ``catkin_make``
2. 刷新环境变量： ``source devel/setup.bash``
3. 根据你想运行的功能：
    - 若要自主建图：``roslaunch auto_nav auto_slam.launch`` 建图完成后``roslaunch auto_nav save_map.launch``保存地图
    - 若要自主导航：``roslaunch auto_nav clean_work.launch``
    - 若要手动建图：``roslaunch manual_nav slam.launch`` 建图完成后``roslaunch manual_nav save_map.launch``保存地图
    - 若要手动导航：``roslaunch manual_nav nav.launch``

### 参考链接
- [https://github.com/hrnr/m-explore](https://github.com/hrnr/m-explore)
- [https://github.com/peterWon/CleaningRobot](https://github.com/peterWon/CleaningRobot)
- [https://github.com/mywisdomfly/Clean-robot-turtlebot3](https://github.com/mywisdomfly/Clean-robot-turtlebot3)