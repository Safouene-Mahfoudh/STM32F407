The STM32F407VG microcontroller includes three 12-bit analog-to-digital converter (ADC) blocks (ADC1, ADC2 and ADC3). The conversion time for eachADC block is about 1µs.There is a wide variety of possible ADC configurations.The maximum frequency of the analog ADC clock is 36 MHz.

The possibilities of use of an ADC converter are multiple.  
The resolution of the ADC is configurable: 12, 10, 8 or 6 bits.  
The Configuration of an ADC using STM32CubeMX :  
- Activate the ADC clock
- Enable the GPIO clock for the pin you wish to use.
- Configure the GPIO pin as an analog input
- Configure the speed of the ADC

The total conversion time of 12-bit ADC is :  

**Tconv = sampling time + 12 ADCCLK cycles**

Usually simpling time is at least 3 cycles. So at least it will take 15 clock cycles.  

The instructions used to convert an analog input are :  
**HAL_ADC_Start(&hadc1);    
HAL_ADC_PollForConversion(&hadc1, 100) ; // waiting 100 clock cycles  
Valeur_ADC = HAL_ADC_GetValue(&hadc1) ;**

