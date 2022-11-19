# Lab-On-A-Chip
## The code is modified to enable the RP2040 to read the value from the APDS9960 via the PIO

- We first set the color integration time and configure the control register. 
- Later, the light and proximity sensors are enabled, after which we read from the address and write the corresponding data, stored in the uint16_t representation. 
- The mask is later used to check if the prox and color values can be transmitted, after which they are printed on the console. 
  (took help of Ruturaj's implementation for getting an idea)
  
Output:

https://user-images.githubusercontent.com/69215958/202837067-61279c4d-6720-46d8-a24f-c8cc66e26fc9.mp4
