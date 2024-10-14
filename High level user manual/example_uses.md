\page example_uses Example Uses

## Use Case 1: [Setup a VLC link between two ESP32-S3 boards]

1. Connect one of the ESP32-S3 board to a computer.
2. Open the serial communication software (e.g., PuTTY) or use a shortcut, this skips step 3 (see how \ref putty_setup "Serial console with PuTTY").
3. Configure the serial connection settings, or load a saved configuration file:
   - Set the serial line (COM port)
   - Set the speed (baud rate) to 115200
4. Open the connection to the ESP32-S3 board.
5. Set encryption keys, maps, and iterations for secure communication for the Transmission and Reception.
6. Repeat the steps for the second ESP32-S3 board, ensuring the Transmission and Reception settings match the first board's Reception and Transmission, respectively (RX-TX, TX-RX). 
7. Transmission of data between the boards is now possible.
<details>
<summary>Note</summary>
\note The ESP32-S3 boards must be in close proximity for the VLC communication to work.  
The boards can be connected to the same computer or different computers, as long as the serial communication software is configured correctly.  
Ensure that the boards are running the same software version and have the same encryption keys, maps, and iterations set for secure communication.
</details>


## Use Case 2: [Normal VLC communication between two ESP32-S3 boards]

1. After setting up the VLC link between two ESP32-S3 boards, the boards can communicate with each other.
2. Let's say Board 1 wants to send data to Board 2, and vice versa.
  -Board 1: 
      ``` set_encryption TX logistic 0.3445 0.123214 1000 0.61232 0.999 1000```
      ``` set_encryption RX duffing 0.51231 0.5655 1000 0.687 0.899 1000```
   -Board 2:
      ``` set_encryption TX duffing 0.51231 0.5655 1000 0.687 0.899 1000```
      ``` set_encryption RX logistic 0.3445 0.123214 1000 0.61232 0.999 1000```
3. On either of the boards, transmit the data using the `transmit` command.
   ``` transmit "Hello World!"```
4. The data is now transmitted between the boards.
