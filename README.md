
# 1D-Neon
Work Package from an European Project to demonstrate the power generation capacity of the polymer.

## Project Description 

### Contents of this git:
| Folders                              | Description  |
|:-------------------------------------|:-------------|
| firmware/1D_Neon_v1.0.X| Project final code source folder. |
| firmware/1DNEON_Demo.X| Project old code source folder.|
| hardware/1DNEON_PCB_v1.0 | Folder containing PCB design files. |

## Project Structure

### MPLAB X IDE
Using a PIC18F27K42.

#### I2C1
| Item| Format|Units| Remarks|
|:-------|:-------------|:-------|:-------------|
|Clock	|100|KHz| -	|
|Fast Mode	|Disable|-| -	|

##### GPIO
| Pin| Module|Function|Description| WPU| OD|
|:-------|:-------------|:-------|:-------------|:-------------|:----|
|RA2|Digital Output|LED - Color|Interface Led|-|-|
|RA3|Digital Output|LED - Color|Interface Led|-|-|
|RA4|Digital Output|LED - Color|Interface Led|-|-|
|RA5|Digital Output|LED - Color|Interface Led|-|-|
|RC0|ADCC|Sens|ADC aquisition pin|-|-|
|RC1|Digital Output|RST|Reset pin Oled|-|-|
|RC2|Digital Output|DC|DC pin Oled|-|-|
|RC3|I2C1|SCL| I2C clock |-| X|
|RC4|I2C1|SDA| I2C data |-|X|

The microcontroller uses the ADCC peripheral to acquire the voltage values at the ends of the polymer sleeve, over a period of time. Then it goes through an algorithm that allows to obtain the number of voltage peaks. This value is saved and its display to the user interface. To perform the display control, the library [U8G2](https://github.com/CENTITVC/API-S/tree/master/Display%26LED/U8G2) was used.
There is a light interface that is controlled by the GPIO pins of the microcontroller and that allows to perform a state interaction with the user.

## Authors 
* **André Leite**
* **José Matos** 
* **Helena Fernandes**
