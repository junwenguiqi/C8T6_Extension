# STM32C8T6 Extension Board
The main circuit of this board is divided into two parts: the power circuit and the control circuit.

## Power Circuit
1. The power is divided into two branches: power supply for the motor module and power supply for other components.
2. **Motor Module Power Supply**: The motor is provided with two operating power options: 5V (VCC → LM2596-5.0) and VCC (direct battery connection). The power level can be switched via the terminal block next to the TB6612 on the board. The motor module interface connects to the TB6612 module.
3. **Other Power Supply**: Uses LM2596-5.0 + AMS1117-3.3 to supply power to various modules and the STM32.

## Control Circuit
Various functional module interfaces have been adapted, mainly including:
- I2C communication OLED
- Bluetooth HC-05
- 4 push buttons
- Voltage detection with ADC function
- Ultrasonic module
- Buzzer
- UART2 serial port
- MPU6050 module
- 2 I/O LEDs

## TODO
1. The copper traces at the power interface on the PCB are relatively thin. For high current applications, the copper foil area or trace width needs to be increased.
2. Regarding power supply filtering capacitors: tantalum capacitors are currently used. If you don't have them on hand and need to quickly verify functionality, they can be replaced with standard ceramic capacitor packages.
