# Kcalibrator
Alternative K-factor calibration pattern generator.
Should provide better (or at least different) way to calibrate Liniar Advance (and similar algorythms) than default Marlin K-factor Calibration Pattern (https://marlinfw.org/tools/lin_advance/k-factor.html)

## Requirements
Requires Python 3 to run.
No additional packages except the Standard Library required.

## Usage
A script with a simple interface. The setting is carried out by changing the parameters in the configuration file or in the program interface.
Configure the script and run it with Python - it will generate an output G-code file in the working directory.

User can adjust:
- Basic machine parameters (bed size, filament diameter, autoleveling, etc.)
- Basic printing settings (temperature, cooling, retraction, etc.)
- Pattern parameters (size, speeds, K-factor range and step, number of perimeters, number of layers prited with each specific K-factor, etc.)

Pattern consists of a rectangular wall (or two) printed with sharp changes in speed and with K-factor increasing from bottom to top.
Print the pattern and find the height where it looks the best. Corners should not bulge, flow should be homogeneous with as little influence from speed changes as possible, seam should be barely noticeable. Calculate desired K-factor from this height and parameters you used to generate the pattern

## Good luck!
