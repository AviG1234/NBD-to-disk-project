# NBD-to-disk-project

## Overview

This project demonstrates Linux file systems that operate in userspace. The core functionality involves establishing a connection to a network block device (NBD) and utilizing the program's memory as a block device (disk). Storage management is facilitated through the IStorage interface class, providing flexibility for replacement or customization according to specific requirements.

## Request Engine Framework

- **FW Overview:**
  The FW created as a class OOD project using several classic dising patterns. the linux oreated fw monitors file discriptors and handels events in a cofigereble way.
  the FW oalsow give logging and p&p serveces. 

- **FW cofigering and Activation:**
  

## Example:
```c
#include "watchdog.h" 

int main(int argc, char **argv) {
    // Activate the watchdog with parameters
    status_ty status = MakeMeImmortal(3, 10, "/watchdog_files/wd_process", argv);

    if (status == ACTIVATION_SUCCESS) {
        // Your program logic here

        // Terminate the watchdog when your program finishes
        DoNotResuscitate();
    } else {
        // Handle activation failure
        fprintf(stderr, "Watchdog activation failed.\n");
    }

    return 0;
}

```

## Build and Test:
Compile your watchdog program using your preferred compiler. Additionally, 
a test file named usr_wd_test.c is provided for testing purposes
### Build
-Wl,-rpath=./watchdog_files/ -ansi -pedantic-errors -Wall -Wextra -DNDEBUG -O3 -o test_watchdog usr_wd_test.c ./watchdog_files/watchdog.a ./watchdog_files/lib_release_ds.so -Iwatchdog_files -ldl

### Run
./test_watchdog
