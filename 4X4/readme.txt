microcontroller: ch32v203g6u6
board: lana-tny-01
microcontroller manufacturer: wch
board manufacturer: wch
icon: icons/folder/closed/blinky.png
link: https://embeetle.com/#supported-hardware/wch/boards/lana-tny-01


info:
This project was originally a WCH Eclipse sample project which we've slightly
modified to fit the typical Embeetle project structure.

The original resources can be found on:
http://www.wch-ic.com/products/CH32V203.html

The ZIP-folder is not downloadable on that page. Refer to:
https://www.wch.cn/downloads/CH32V20xEVT_ZIP.html

After unzipping this ZIP-folder:
  - The general source code is copied from: 'CH32V20xEVT/EVT/EXAM/SRC/'.
  - The sample projects are in folders like: 'CH32V20xEVT/EVT/EXAM/GPIO/GPIO_Toggle/User/'.
  - The linkerscript is found at: 'CH32V20xEVT/EVT/EXAM/SRC/Ld/Link.ld'.


SAMPLE PROJECTS
---------------
Samples
   |-- ADC
   |      |-- ADC_DMA: ADC DMA sampling routines
   |      |-- AnalogWatchdog: analog watchdog routine
   |      |-- Auto_Injection: automatic injection mode routine
   |      |-- Discontinuous_mode: discontinuous mode routine
   |      |-- DualADC_AlternateTrigger: dual ADC alternate trigger sampling routine, only applied to CH32V20x_D6 
   |      |-- DualADC_Combined_RegInjectionSimul: dual ADC combined regular + injection + simultaneous sampling routine, only applied to CH32V20x_D6
   |      |-- DualADC_FastInterleaved: dual ADC fast interleaved sampling routine, only applied to CH32V20x_D6
   |      |-- DualADC_InjectionSimul: dual ADC injection simultaneous sampling routine, only applied to CH32V20x_D6 
   |      |-- DualADC_RegSimul: dual ADC regular simultaneous sampling routine, only applied to CH32V20x_D6
   |      |-- DualADC_SlowInterleaved: dual ADC slow interleaved sampling routine, only applied to CH32V20x_D6
   |      |-- ExtLines_Trigger: external lines trigger ADC conversion routine
   |      |-- Internal_Temperature: internal temperature sensor routine 
   |-- BLE: only for CH32V20x_D8W 
   |      |-- BackupUpgrade_IAP: backup wireless upgrade IAP routine. Detect the current code flag, determine whether to move the code from the backup area to the user area, and run the code in the user area 
   |      |-- BackupUpgrade_OTA: backup wireless upgrade user routine. Add OTA function to peripheral slave routines, save the upgrade firmware to the backup area and jump to the IAP program to upgrade 
   |      |-- BLE_UART: BLE and UART transparent transmission routine, for detailed instructions, please refer to the <description.txt> document in the root directory
   |      |-- BLE_USB: BLE with USB routine, USB emulation 340 device forwards BLE data 
   |      |-- Broadcaster: broadcaster routine, always broadcast when in broadcast status
   |      |-- CentPeri: central-peripheral routine, integrate the function of central routine and peripheral routine and run simultaneously
   |      |-- Central: central routine, actively scan surrounding devices, conect to the specified peripheral address, search custom service and characteristic, execute read/write commands, peripheral routine is needed, and modify the peripheral address to the routine target address, (84:C2:E4:03:02:02) by default
   |      |-- CyclingSensor: cycling sensor routine, upload speed and cadence regularly after connected to the host
   |      |-- DirectTest: direct test routine, test data packets sent by specified communication channel
   |      |-- HAL: Hardware-related files shared by routines
   |      |-- HeartRate: heart rate routine, upload heart rate regularly after connected to the central
   |      |-- HID_Consumer: BLE consumer routine, simulate user control device, upload volume key down key regularly after connected to the central
   |      |-- HID_Keyboard: BLE keyboard routine, simulate a keyboard device, upload key value regularly after connected to the central
   |      |-- HID_Mouse: BLE mouse routine, simulate a mouse device, upload key value regularly after connected to the central
   |      |-- HID_Touch: BLE touch routine, simulate a touch pencil device,  upload touch value regularly after connected to the central
   |      |-- LIB: BLE protocol stack library file and header file
   |      |-- LWNS: LWNS wireless networking routine,including broadcast, unicast, netflood, mesh.
   |      |-- MultiCentPeri: Multi-central and multi-peripheral routines, support connecting three masters and three slaves at the same time
   |      |-- MultiCentral: multicentral routine, actively scan surrounding devices, conect to the specified three peripheral addresses, search custom services and characteristics, execute read/write commands, peripheral routine is needed, and modify the peripheral address to this routine target address, the addresses of these peripherals are (84:C2:E4:03:02:02), (84:C2:E4:03:02:03) and (84:C2:E4:03:02:04) by default
   |      |-- Observer: observer routine, scan regularly, print the scanned broadcast address if the scanning result is not empty
   |      |-- OnlyUpdateApp_IAP: the only library wireless upgrade IAP routine, with OTA function, upgrade the user area code after receiving the upgraded firmware
   |      |-- OnlyUpdateApp_Peripheral: the only library wireless upgrade user routine, on the basis of peripheral routine, the jumping to IAP program is added for subsequent upgrades
   |      |-- Peripheral: peripheral role routine, custom including five services with different  attributes, including read attribute, write attribute, notify attribute, read/write attribute, and safe and readable attribute
   |      |-- peripheral_ancs_client: peripheral slave role routine, including Apple Notification Center service
   |      |-- peripheral_ETH: Bluetooth ETH routines
   |      |-- RF_PHY: non-standard wireless transceiver routines
   |      |-- RF_PHY_Hop: non-standard wireless frequency hopping transceiver routine
   |      |-- RunningSensor: running sensor routine,upload rate regularly after connected to the central 
   |      |-- SpeedTest_Central: Bluetooth speed test central routine
   |      |-- SpeedTest_Peripheral: Bluetooth speed test peripheral routine
   |      |-- SYNC_ADV: cycle synchronization advertising routine
   |      |-- SYNC_SCAN: cycle synchronization scanning routine
   |      |-- WCH BLE Software Developers Guide.pdf
   |      |-- BLE Certification: Product: WCH CH32V208 QDID: 179771  
   |      |-- MESH
   |             |-- adv_ali_light: Tmall Genie light routine, devices can be found and provisioned network via Tmall Genie, to control the switch state. By default, only switch attribute can be controlled. If other attributes (brightness, power, temperature, etc.) are needed, add the corresponding processing function and status report function according to the attribute description of the Alibaba Cloud product configuration.
   |             |-- adv_ali_light_add_lightness: MESH general attribute adding routine. On the basis of the Tmall Genie light routine, the brightness attribute is added, which is used to compare the original Tmall Genie light routine to quickly become familiar with the method of adding other MESH general attributes.
   |             |-- adv_ali_light_add_windspeed: Tmall definition attribute adding routine. On the basis of the Tmall Genie light routine, the wind speed attribute is added, which is used to compare the original Tmall Genie light routine to quickly become familiar with the method of adding other Tmall definition attributes.
   |             |-- adv_ali_light_multi_element: Multi-element fan lamp, which is used to compare the original Tmall Genie light routine to quickly become familiar with the method of adding multi-element Tmall definition attributes.
   |             |-- adv_ali_light_with_peripheral: Based on the Tmall Genie light routine, add brightness and color temperature controls, it supports the connection control of BLE debugging tool on the mobile phone.
   |             |-- adv_proxy: proxy node routine, which can be used to provision network through the PV_GATT layer (BLE connection).
   |             |-- adv_vendor: vendor-defined model routine, used with self_provisioner_vendor, supports two communication attributes of response transmission and non-response transparent transmission, and develops the communication protocol by yourself.
   |             |-- adv_vendor_friend: based on vendor-defined model routine, support friend node function
   |             |-- adv_vendor_low_power: On the basis of the vendor custom model routine, support low-power node functions and should be used with friend nodes
   |             |-- adv_vendor_self_provision: On the basis of the vendor custom model routine, support local provision
   |             |-- adv_vendor_self_provision_IAP: MESH backup wireless upgrade IAP routine, detect the current code flag, judge whether to move the backup area code to the user area and run the user area code
   |             |-- adv_vendor_self_provision_with_peripheral: MESH backup wireless upgrade user routine, On the basis of the vendor custom model routine, supports the connection control of the mobile phone BLE debugging assistant, receives the distribution network information through BLE and distributes the network itself. It is suitable for terminal control networking applications. It can formulate the communication protocol by itself to realize the mobile phone control all devices in the mesh network.
   |             |-- self_provisioner_vendor: vendor-defined model self-provisioning network initiator routine, used with adv_vendor, automatically provision network to the surrounding devices without network, and add it to its own mesh network, support provision network to six devices by default . The default configuration device is bound with single APPKEY, which is used for response transmission and non-response transparent transmission, and the configuration device is bound with single subscription address, which is used for mass sending of unanswered messages
   |             |-- self_provisioner_vendor_with_peripheral: Based on the vendor-defined model self-provisioning network initiator routine, can be connected and controlled by BLE debugging tool on the mobile phone, transfer the communication between the mobile phone and the mesh network, and can draw up the communication protocol to implement that all devices in mesh network can be controlled the mobile phone.
   |             |-- MESH_LIB: MESH protocol stack library file and header file
   |             |-- Qinheng MESH APP Management Distribution Network Application Manual.pdf
   |             |-- Qinheng Low Energy Bluetooth MESH Software Development Reference Manual.pdf
   |-- BKP: BKP routine
   |-- CAN: only for CH32V20x_D6-CH32V20x_D8W 
   |      |-- Networking: CAN routine: normal mode, standard frame and expanded frame data transceiver
   |      |-- TestMode: test mode, including silent mode, loopback mode and loopback silent mode
   |      |-- Time-triggered: time triggered communication mode   
   |-- CRC: CRC routine
   |-- DMA
   |      |-- DMA_MEM2MEM: Memory to memory mode routine
   |      |-- DMA_MEM2PERIP: Memory to peripheral mode, and peripheral to memory mode routine, see peripheral sub-routines
   |-- ETH: only for CH32V20x_D8-CH32V20x_D8W
   |      |-- 1_Tool_Doc: routine-related documents and configuration software
   |      |-- DHCP: DHCP demonstration routine to obtain IP automatically, and establish TCP connection for data return
   |      |-- DNS: DHCP demonstration routine to obtain IP automatically and then request domain name resolution 
   |      |-- ETH_CFG: ETH_CFG routine. Create a UDP Server to communicate with upper computer, to configure WCHNET functions, including configuring various parameters and creating a new communication. 
   |      |-- ETH_IAP: ETH IAP routine
   |      |-- ETH_UART: ETH_UART routine, to demonstrate data transparent transfer between Ethernet and UART. By default, the 1000000 baud rate (can be modified in bsp_uart.h) is selected for serial port data transmission
   |      |-- IPRaw_PING: PING function demonstration routine
   |      |-- Mail: to demonstrate reception and transmission of SMTP and POP3 mails 
   |      |-- MQTT: MQTT routine, to demonstrate MQTT protocol communication based on TCP/IP   
   |      |-- NetLib: Network protocol stack library file
   |      |-- TcpClient: demonstration routine that TCP client receives data after connected to the server and then returns data 
   |      |-- TcpServer: demonstration routine that TCP server receives data after connected to the client and then returns data
   |      |-- UdpClient: demonstration routine that Udp Client receives data and returns data
   |      |-- UdpServer: demonstration routine that Udp Server receives data and returns data
   |      |-- WebServer: Web Server routine, to demonstrate the configuration of WCHNET device functions through Web browser. As the WCHNET devices have built-in web server, the network parameter configuration and password management of WCHNET can be implemented on the web page.   
   |-- EXTI: external interrupt line routine
   |-- FLASH: FLASH erase/read/write, and fast programming
   |-- FreeRTOS: FreeRTOS migration routine 
   |-- GPIO: GPIO routine
   |-- HarmonyOS: HarmonyOS migration routine  
   |-- I2C
   |      |-- I2C_7bit_Mode: 7-bit addressing mode, master/slave mode, transceiver routine
   |      |-- I2C_10bit_Mode: 10-bit addressing mode, master/slave mode transceiver routine
   |      |-- I2C_DMA: I2C DMA, master/slave mode transceiver routine
   |      |-- I2C_EEPROM: I2C interface routine to operate EEPROM peripheral 
   |      |-- I2C_PEC: PEC error check, master/slave mode transceiver routine
   |-- INT
   |      |-- Interrupt_VTF: VTF IRQ interrupt routine   
   |-- IAP: IAP upgrade routine, including the Hex to Bin tool and IAP upgrade tool  
   |      |-- USB_UART: USB+UART IAP routine    
   |-- IWDG: independent watchdog routine
   |-- OPA: OPA4 as voltage follower output routine
   |-- PWR
   |      |-- Sleep_Mode: low power, sleep mode routine
   |      |-- Standby_Mode: low power, standby mode routine
   |      |-- Stop_Mode: low power, stop mode routine
   |      |-- Standby_RAM_LV_Mode: when LV is enabled in standby mode, RAM 2k and 30K low-power data holding routines
   |      |-- Standby_RAM_Mode: when LV is not enabled in standby mode, RAM 2k and 30K low-power data holding routines
   |-- RCC
   |      |-- Get_CLK: Get system-HCLK-AHB1-AHB2 clock routine   
   |      |-- MCO: MCO pin clock output routine
   |      |-- HSI_PLL_Source: HSI or HSI/2 as PLL input clock routine       
   |-- RT-Thread: RT thread migration routine 
   |-- RTC: calendar routine
   |-- SPI
   |      |-- 1Lines_half-duplex: single wire half duplex mode, master/slave mode, data transceiver
   |      |-- 2Lines_FullDuplex: two-wire full duplex mode, master/slave mode, data transceiver
   |      |-- FullDuplex_HardNSS: Hardware NSS mode, master/slave mode, data transceiver
   |      |-- SPI_CRC: CRC error check and master/slave mode transceiver routine
   |      |-- SPI_DMA: SPI DMA, master/slave mode transceiver routine
   |      |-- SPI_FLASH: SPI interface operation flash peripheral routine
   |-- TencentOS: TencentOS migration routine     
   |-- TIM
   |      |-- Clock_Select: clock source selection routine
   |      |-- ComplementaryOutput_DeadTime: complementary output and deadband insertion mode routines
   |      |-- ExtTrigger_Start_Two_Timer: external trigger routines to start two timers synchronously
   |      |-- Input_Capture: input capture routine
   |      |-- One_Pulse: single pulse output routine
   |      |-- Output_Compare_Mode: output comparison mode routine
   |      |-- PWM_Output: PWM output routine
   |      |-- Synchro_ExtTrigger: slave mode routine, including reset mode, gating mode and trigger mode
   |      |-- Synchro_Timer: timer synchronization mode
   |      |-- TIM_DMA: timer DMA routines
   |-- TOUCHKEY: touchkey detection routine
   |-- USART
   |      |-- USART_DMA: USART DMA, master/slave mode transceiver routine
   |      |-- USART_HalfDuplex: single wire half duplex mode, master/slave mode transceiver routine
   |      |-- USART_HardwareFlowControl: hardware flow control mode, master/slave mode, transceiver routine
   |      |-- USART_Interrupt: USART interrupt routine, master/slave mode transceiver routine
   |      |-- USART_MultiProcessorCommunication: multiprocessor communication mode routine
   |      |-- USART_Polling: polling transceiver mode, master/slave transceiver routine
   |      |-- USART_Printf: USART Print debugging routine
   |      |-- USART_SynchronousMode: synchronous mode, master/slave mode, transceiver routine
   |-- USB
   |      |-- USBD
   |      |      |-- CH372: Simulates a custom USB device (CH372 device) with endpoints 1, 3 down and 2, 4 up. Data down from endpoint 1 is uploaded from endpoint 3 and not reversed, and data down from endpoint 2 is uploaded from endpoint 4 and reversed.
   |      |      |-- Compatibility_HID: Simulates HID devices, with data transmitted up and down through the serial port.
   |      |      |-- CompositeKM: Simulate keyboard and mouse, use IO to simulate keystrokes, while simulated data can be uploaded through serial port 2.
   |      |      |-- MSC_U-Disk: Smulates a simple USB flash drive, optionally using on-chip Flash or external SPI-Flash
   |      |      |-- MSC_CD-ROM: Simulate CDROM, need external SPI-Flash
   |      |      |-- SimulateCDC: Simulate a CDC serial port and use serial port 2 to send and receive.
   |      |      |-- SimulateCDC-HID: Simulate a CDC serial port, use serial port 2 to send and receive, HID interrupt endpoints to send and receive data to reverse and upload.  
   |      |-- USBFS
   |             |-- DEVICE
   |             |      |-- CH372: Simulates a custom USB device (CH372 device) with endpoints 1, 3 down and 2, 4 up. Data down from endpoint 1 is uploaded from endpoint 3 and not reversed, and data down from endpoint 2 is uploaded from endpoint 4 and reversed.
   |             |      |-- Compatibility_HID: Simulates HID devices, with data transmitted up and down through the serial port.
   |             |      |-- CompositeKM: Simulate keyboard and mouse, use IO to simulate keystrokes, while simulated data can be uploaded through serial port 2.
   |             |      |-- MSC_U-Disk: Smulates a simple USB flash drive, optionally using on-chip Flash or external SPI-Flash
   |             |      |-- MSC_CD-ROM: Simulate CDROM, need external SPI-Flash
   |             |      |-- SimulateCDC: Simulate a CDC serial port and use serial port 2 to send and receive.
   |             |      |-- SimulateCDC-HID: Simulate a CDC serial port, use serial port 2 to send and receive, HID interrupt endpoints to send and receive data to reverse and upload.  
   |             |-- HOST_IAP
   |             |      |-- APP: APP used with HOST_IAP, the project has modified the starting location of the program, after compilation, you need to convert the file into a bin file and rename it to APP.bin
   |             |      |-- HOST_IAP:  The host U disk IAP routine based on the U disk read file routine finishing, read the file with the name bit APP.bin from the U disk, write it to the internal flash, check it and jump automatically.
   |             |-- HOST_KM: The host operates the keypad, gets the data of the endpoints uploaded by the keypad and prints it, supports U-port under level 1 hub
   |             |-- HOST_MTP_FileSystem: Enumeration process of a USB host to a device that supports MTP and PTP protocols, supports MTP and PTP protocols, and reads its files
   |             |-- Host_Udisk: USB host operation USB disk routine 
   |             |-- Udisk_Lib: U disk file system library file     
   |-- WWDG: window watchdog routine