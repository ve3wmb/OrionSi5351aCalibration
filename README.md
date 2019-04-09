# OrionSi5351aCalibration
Si5351a calibration code using SoftWire (software I2C interface) and NeoSWSerial. 

This code is based on the Etherkit Si5351 Library SI5351 Calibration sketch in the Etherkit Si5351 examples folder. 
The sketch outputs a 10Mhz calibration signal on CLK0 (configurable in the code) and utilizes user input
via single character commands entered through the Arduino Serial Monitor (9600 baud) to correct the
output frequency (measured manually via frequency counter). When the user types 'q' to terminate the calibration
the sketch will output an int32_t value (positive or negative) that is then can be used for SI5351A_CLK_FREQ_CORRECTION 
for the Orion WSPR Beacon (in the file OrionXConfig.h within the OrionWSPR project in GITHUB). 
