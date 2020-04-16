## MLX90640_micropython
A quick and dirty re-purposing of adafruit circuitpython library for MLX90640 IR sensor so that it can be read using micropython (e.g. pycom's wipy 3.0)

# What was done:
Using a raspberry pi 3b running Raspbian 10 (buster), the adafruit_mlx90640 python library (and all dependencies) was installed in a target folder (e.g. "/home/pi/tgt_folder") using pip3. The IR sensor was tested on this raspberry pi using a basic example codes shown here: https://github.com/adafruit/Adafruit_CircuitPython_MLX90640

Once it was tested that the sensor was working correctly using the drivers in the target folder, the contents of this target folder was copied over to the "lib" folder of the PyCom WiPy 3.0. Most of the imports in the original circuitpython implementation are not required for WiPy micropython (like board id checks, modules like threading etc.) and has hence been disabled/deleted for easy debugging and readability. 
