## [Communication Circuit](#communication-circuit)
To control the Dynamixel actuators, the main controller needs to convert its UART signals to the half duplex type. The recommended circuit diagram for this is shown below.

### TTL Communication
![](/assets/images/dxl/ttl_circuit.png)

![](/assets/images/dxl/x/x_series_ttl_pin.png)

### RS-485 Communication
![](/assets/images/dxl/x/x_series_485_circuit.jpg)

![](/assets/images/dxl/x/x_series_485_pin.png)

The power of Dynamixel is supplied via Pin1(-), Pin2(+).  
(The above circuit is built into Dynamixel-only controller.)  
In the above circuit diagram, the direction of data signal of TxD and RxD in the TTL Level is determined according to the level of DIRECTION 485 as follows:  
In case of DIRECTION485 Level = High: The signal of TxD is output to D+ and D-  
In case of DIRECTION485 Level = Low: The signal of D+ and D- is output to RxD  

{% include en/dxl/pinout_warning.md %}
