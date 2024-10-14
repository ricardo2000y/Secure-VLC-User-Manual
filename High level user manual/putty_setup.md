\page putty_setup Serial console with PuTTY

### Installing PuTTY

1. Download PuTTY from the [official website](https://www.putty.org/).
2. Run the installer and follow the prompts.

### Configuring PuTTY

1. Open PuTTY.
2. Set the Connection type to **Serial**.
3. Configure the connection:
   - Set the serial line (COM port)
   - Set the speed (baud rate) typical value is 115200
   
   <details>
   <summary>Note</summary>
   
   \note
        On Windows, find the COM port in Device Manager under "Ports (COM & LPT)".
   
   </details>

4. Save the configuration file with a descriptive name (e.g., "VLC_console").
5. Create a shortcut to this configuration file:
     "C:\Program Files\PuTTY\putty.exe" -load "VLC_console"
        <details>
        <summary>Note</summary>
        \note
        Format:  
                 `"[path to executable]" -load "[name of the saved configuration]"`
        
        </details>

6. Launch the console for communication between the computer and the ESP32-S3 by either:
- Launching the shortcut, or
- Opening PuTTY and loading the configuration, and selecting 'Open'.


### Connecting to the ESP32-S3


- Launch the created shortcut .  
- Or, follow these steps:
1. Open PuTTY and load the saved configuration file
2. Click 'Open' to start the connection.



\image html "C:\Users\sampa\Dropbox\Tese\Software Tese\User manual\High level user manual\putty_screenshot.png" "PuTTY Configuration Screen"