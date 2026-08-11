# Project for basic control of an LCD display with an STM32 using the I2C protocol.

For controlling an I2C display with an STM32, follow the steps below:

1. Enable the I2C communication of the STM32 over STM32CUBEMX, which is under the "Connectivity" drop down in the left side menu.
2. Connect the SDA and SCL pins of the STM32 and the LCD Display.
3. Copy the Core/Src/liquidcrystal_i2c.c to your Core/Src directory
4. Copy the Core/Inc/liquidcrystal_i2c.h to your Core/Inc directory
5. In the liquidcrystal_i2c.h file, set the line 4 to include the HAL for the specific MCU you are using.
6. In the main.c file, set the line 24 to include the HAL for the specific MCU you are using.

Note: If you started your own project, your CmakeLists.txt wont have the target sources and target include directories for the library configured,
so, your code will not compile.
In that case:
1. put `Core/Src/liquidcrystal_i2c.c` inside of `target_sources`
2. put `Core/Inc` inside of `target_include_directories`

After these steps, compile your code, and flash it to your microcontroller. The display should run.
 
![lcd_i2c_setup_photo.jpeg](https://raw.githubusercontent.com/bosdos12/I2C_LCD_stm32f103c8t6/refs/heads/main/Images/lcd_i2c_setup_photo.jpeg)
![lcd_i2c_screenshot_saleae.jpeg](https://raw.githubusercontent.com/bosdos12/I2C_LCD_stm32f103c8t6/refs/heads/main/Images/lcd_i2c_screenshot_saleae.jpeg)
