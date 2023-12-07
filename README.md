# NBD-to-disk-project

## Overview

This project demonstrates Linux file systems that operate in userspace. The core functionality involves establishing a connection to a network block device (NBD) and utilizing the program's memory as a block device (disk). Storage management is facilitated through the IStorage interface class, providing flexibility for replacement or customization according to specific requirements.

## Request Engine Framework
  - The framework (FW) is crafted as a class-oriented object-oriented design (OOD) project, employing various classic design patterns. In the Linux-oriented framework, file descriptors are continuously monitored, and events are handled in a configurable manner. Additionally, the framework provides logging capabilities and services for plug-and-play (P&P) functionality.
  - A more simple demonstration of the FW is shown in the repository: XXXX
  - Log of the runing programs errors is stord at ./log/logfile.log, in order to record all operations not only errors use uncoment the SetLogLevel method in ./test/request_enginefw_test.cpp main function.
  - Using  plug-and-playfunctionality is dun by moving a shard obgect (.so file) to the ./plugins directory. 


## Build and Run:
### Building the Code
  - Compile the program in debug (-g) mode using '$ make' commend or without using '$ make MODE=GC'

### Running the Example Code:
  -  Start by compileng the code by entering commend '$ make' to terminal. 
