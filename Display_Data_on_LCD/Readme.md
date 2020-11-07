##There are several varieties of LCD's, they differ with the number of lines and the number of columns. On the other hand,they also differ with the pin-out and the type of connection to the control.

- Normal mode: 8 bits or 4 bits with RS and E control bits.
- I2C mode
- SPI mode
- Serial LCD mode

##We will use the LCD serial mode which only requires 3 wires: Vcc, GND and RX.
##The TX output of the UART3: Pin PB10/ TX will be used to send the commands as follows than the data to be displayed on the LCD.
##To send a command to our LCD, we will use the following command:

***HAL_UART_Transmit(&huart3, (uint8_t *)cursor_home, 2, 0xFF);***

##The cursor_home variable will be declared as follows:

***uint8_t curseur_home[2]={0xFE,0x46};***

##To send text or the value of any variable, just use **printf**
