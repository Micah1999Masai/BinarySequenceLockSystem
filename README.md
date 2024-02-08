# Gottcha Anti-Theft Machine FSM Project

## Overview
This repository contains the design and testing documentation for the Gottcha Anti-Theft Machine, a Finite State Machine (FSM) developed for the CS 370 Computer Architecture course at San Diego State University. The machine is designed to detect a specific 8-bit binary sequence, serving as an anti-theft mechanism for vehicles.

## Repository Structure
- `16-bit lock.cct`: LogicWorks circuit file showcasing the FSM with a 16-bit input buffer.
- `16-bit lock.pdf`: Visual representation of the circuit for those without LogicWorks.
- `BinarySequenceLockSystemTesting.cct`: Test suite demonstrating the FSM's response to various inputs.
- `LockSystemFinal.pdf`: Complete circuit diagram of the FSM.
- `StateDiagram&Table,K-maps&equations.pdf`: Detailed documentation of the state diagram, state table, Karnaugh maps, and derived Boolean equations.
- `Anti-Theft test video.mp4`: A video demonstrating the testing and functionality of the lock system.

## Features
- **Factory Preset Model**: FSM with a preset secret key for authentication.
- **16-bit Lockout Mechanism**: Security feature that disables the system after 16 consecutive incorrect bits, requiring a reset to continue.
- **Reset Functionality**: Allows the system to be reset and ready to accept new input sequences.

## Installation
To view and interact with the project files:
1. Clone the repository to your local machine.
2. Install [LogicWorks](http://www.logicworks.com) if you wish to run `.cct` files.
3. Open PDF documents with any standard PDF viewer.
4. Play the test video with a media player supporting MP4 format.

## Usage
To understand and interact with the project:
1. Review the PDFs for a visual representation of the circuits and logic design.
2. Explore the .cct files using LogicWorks for an interactive experience.
3. Watch the Anti-Theft test video to see the system in action.

## Testing Scenarios and Video Demonstration
Refer to `BinarySequenceLockSystemTesting.cct` for testing protocols and `Anti-Theft test video.mp4` for a visual walkthrough of the tests. The documentation ensures that the system's operation can be fully understood and verified without direct access to LogicWorks.

The provided video, "Anti-Theft test video", showcases the following test cases for the FSM:
1. Correct Key Entry: Input of the correct secret key '01010100' successfully unlocks the system, resulting in an output of '1'.
2. Extended Key Entry: A longer sequence containing the key '000001010100' also unlocks the system, demonstrating the ability to recognize the key within a continuous input stream.
3. 16-bit Lockout Test: An input of '1111111111101010100', which is longer than 16 bits and ends with the correct key, does not unlock the system. This validates the 16-bit lockout feature, ensuring security even when the key is entered beyond the 16-bit window.
4. Near-Miss Key Entry: The sequence '111101010100' is tested to confirm that the system correctly identifies and unlocks with the correct key embedded in a sequence of inputs.

These test cases ensure the robustness of the FSM against various input patterns and validate the implementation of the lockout mechanism.

## Acknowledgements
- San Diego State University
- CS 370 Instructor Tao Xie