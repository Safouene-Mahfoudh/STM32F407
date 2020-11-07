##In main.c , the LED can be switched ON or OFF with the command :

**HAL_GPIO_WritePin( GPIO TypeDef* GPIOx, uint16_t GPIO_Pin, GPIO_PinState PinState)**

##**GPIOx** : x the port name of the STM32F40xx (from A ... I )
##**GPIO_Pin** specifies the pin of the GPIO_PIN_x port from (0 ... 15)
##**PinState** can be either GPIO_PIN_RESET or GPIO_PIN_SET

##The syntax of the command to switch ON the diode on pin PD12 is :

**HAL_GPIO_WritePin(GPIOD,GPIO_PIN_12,GPIO_PIN_SET);**

##To make this diode blink, we write :
**HAL_GPIO_TogglePin(GPIOD,GPIO_PIN_12);**

##We must add a wait to see the blinking with :
**HAL_Delay(500); // 500 ms**
