# carla-setup
This README file serves the purpose of documenting the process of setting [Carla Driving Simulator](https://carla.org/) as well as a activity log for my Final Year Project titled "Driving Behaviour Analysis at Yellow Light Intersection". 

--------

<br>

# Setting up with Keyboard Controls 
NOTE: Starting Carla requiring at least 2 terminals, with one acting as the server whereas another as the client. More terminals can be added a configuration to the server. 

1. Enter the Carla Virtual Environment within the system. <br>
    `C:\Users\drivesim\carla-env\Scripts\activate.bat`
3. CD into the folder that contains Carla. <br>
    `cd C:\Users\drivesim\Carla Quick Start\WindowsNoEditor`
5. Start the server. (This terminal is your server) <br>
    `CarlaUE4.exe`
7. Open another terminal. Enter the carla venv. (This terminal is your client) <br>
    `C:\Users\drivesim\carla-env\Scripts\activate.bat`
9. CD into the folder that contains the Python scripts. <br>
    `cd C:\Users\drivesim\Carla Quick Start\WindowsNoEditor\PythonAPI\examples`
11. Run the Python file. <br>
    `.\manual_control.py `

<br>

# Setting up with Steering Controls
NOTE: This section is written based on the Logitech G29 Steering Wheel. 

## Creating wheel_config.ini
1. Create a "wheel_config.ini" in the folder that contains all Python scripts. 
2. The contents of the *ini* file is as shown. <br>
    [G29 Racing Wheel] <br>
    steering_wheel=0 <br>
    clutch=3 <br>
    throttle=1 <br>
    brake=2 <br>
    handbrake=4 <br>
    reverse=5
4. Change parameters of the *manual_control_steeringwheel.py*. <br>
    `self._parser.read('file_path/wheel_config.ini')`

<br>

## Steering Wheel Controls
Repeat Steps 1-5 of Setting up with Keyboard Controls. <br>
NOTE: Steps 1-3 can be skipped if server has already been started. <br> <br>
For Step 6, run the Python file. <br>
    `.\manual_control_steeringwheel.py`

<br>

# Configuring the World 
NOTE: 
1. Each configuration should be a new terminal as the configuration scripts are blocking. 
2. Configuration terminals should only be started after the server has been started. 

1. Enter the carla venv.
    `C:\Users\drivesim\carla-env\Scripts\activate.bat`
3. CD into the folder containing the Python files (including the config. scripts)
    `cd C:\Users\drivesim\Carla Quick Start\WindowsNoEditor\PythonAPI\examples`
5. Run the config. scripts
    6. Traffic Generation 
        `.\generate_traffic.py -n 80`
    8. Weather
        `./dynamic_weather.py`
