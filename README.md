# SmartNavGUI

SmartNavGUI is a Qt-based ROS program with a human-machine interaction interface designed to control a smart car. This project allows users to navigate the car via a GUI and displays a SLAM map, showing the car's current position, speed, and orientation on the map. It supports both ROS1 and ROS2.

## Features

- **Human-Machine Interaction Interface**: Control the smart car through an intuitive GUI.
- **SLAM Map Display**: View real-time SLAM maps to understand the car's surroundings.
- **Real-Time Car Data**: Monitor the car's current position, speed, and orientation.
- **ROS1 and ROS2 Integration**: Seamless integration with both ROS1 and ROS2 for robot control and data visualization.

## Installation

To get started with SmartNavGUI, follow these steps:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/XKHoshizora/SmartNavGUI.git
    cd SmartNavGUI
    ```

2. **Install dependencies**:
    - Ensure you have ROS1 or ROS2 installed on your system. Refer to the [ROS1 installation guide](https://wiki.ros.org/noetic/Installation/Ubuntu) or the [ROS2 installation guide](https://docs.ros.org/en/humble/Installation.html) for instructions. Alternatively, you can use the [auto-ros-installer](https://github.com/XKHoshizora/auto-ros-installer.git) project for one-click installation.
    - Install Qt and other required packages:
        ```sh
        sudo apt-get install qt5-default
        ```

3. **Build the project**:
    For ROS1:
    ```sh
    catkin_make
    source devel/setup.bash
    ```

    For ROS2:
    ```sh
    colcon build
    source install/local_setup.bash
    ```

4. **Run the program**:
    For ROS1:
    ```sh
    rosrun smart_nav_gui smart_nav_gui
    ```

    For ROS2:
    ```sh
    ros2 run smart_nav_gui smart_nav_gui
    ```

## Usage

1. Launch the ROS core:
    For ROS1:
    ```sh
    roscore
    ```

    For ROS2:
    ```sh
    ros2 launch <your_launch_file>.launch.py
    ```

2. Start the SLAM node:
    For ROS1 (e.g., using `gmapping`):
    ```sh
    rosrun gmapping slam_gmapping
    ```

    For ROS2 (e.g., using `slam_toolbox`):
    ```sh
    ros2 launch slam_toolbox online_async_launch.py
    ```

3. Launch the SmartNavGUI:
    For ROS1:
    ```sh
    rosrun smart_nav_gui smart_nav_gui
    ```

    For ROS2:
    ```sh
    ros2 run smart_nav_gui smart_nav_gui
    ```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the ROS and Qt communities for their amazing tools and support.
