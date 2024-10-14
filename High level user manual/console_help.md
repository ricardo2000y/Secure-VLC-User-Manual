## Using the ESP32-S3 Console

The ESP32-S3 console provides several commands to interact with the device. Below is a brief overview of each command, including its purpose and usage examples.

### 1. `help`

**Description**: Displays a summary of all registered commands. If a specific command name is provided, it shows detailed information about that command.

**Usage**:
help <command_name>

- **Parameters**:
  - `<command_name>`: (Optional) Name of the command to display detailed information about.
  - If no command name is provided, a list of all registered commands is displayed.

**Example**:
``` help set_encryption```

---

### 2. `set_encryption`

**Description**: Configures encryption variables for the specified map type in TX (transmit) or RX (receive) mode.

**Syntax**:
set_encryption <TX_or_RX> <map_type> <x1> <y1> <iterations1> <x2> <y2> <iterations2>

- **Parameters**:
  - `T` or `TX`: Specifies TX mode.
  - `<map_type>`: Type of map (e.g., duffing(d), logistic(l), 2D-logistic(2)).
  - `<x1>, <y1>`: Coordinates for Map 1.
  - `<iterations1>`: Number of iterations for Map 1.
  - `<x2>, <y2>`: Coordinates for Map 2.
  - `<iterations2>`: Number of iterations for Map 2.

**Example**:
``` set_encryption TX duffing 0.5 0.5 1000 0.6 0.6 1000```

---

### 3. `get_encryption`

**Description**: Retrieves the current encryption variables for either TX or RX mode.

**Syntax**:
get_encryption [TX | RX]

- **Parameters**:
  - `T` or `TX`: Get TX encryption variables.
  - `R` or `RX`: Get RX encryption variables.

**Example**:
``` get_encryption TX```

---

### 4. `transmit`

**Description**: Sends data for transmission.

**Usage**:
transmit <data_to_transmit>

**Example**:
``` transmit Hello World!```

---

### 5. `clear`

**Description**: Clears the console output, providing a clean screen for new commands.

**Usage**:
clear


---

### 6. `freq`

**Description**: Prints the frequency of communication currently being used by the console.

**Usage**:
freq
