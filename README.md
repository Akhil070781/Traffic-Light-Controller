# Four-Way Traffic Intersection Controller

This project involves designing and implementing a Verilog-based controller for a four-way traffic intersection. The primary objective is to ensure that vehicles from only one direction can move at a time, thereby regulating the traffic flow efficiently and safely.

## Project Overview

The traffic controller follows a structured sequence where the traffic light in each direction turns green for 30 seconds, followed by a yellow light for 5 seconds to signal caution. During this time, the traffic lights in the other three directions remain red to prevent any collisions and manage the flow effectively. 

### Key Features

- **Sequential Traffic Light Control**: 
  - **Green Light**: Vehicles are allowed to move for 30 seconds.
  - **Yellow Light**: A 5-second warning period before the light turns red.
  - **Red Light**: Prevents vehicles from moving during the green/yellow phases of the other directions.
  
- **Binary Encoding for Traffic Lights**: 
  - Each traffic light color is assigned a unique binary code, making it easier to identify the current state of each direction's traffic light in the controller logic.
  
- **Synchronization Using Clock Signal**:
  - The system uses a clock signal to synchronize the changes in traffic lights across all four directions, ensuring smooth transitions between green, yellow, and red lights.
  
- **Reset Functionality**:
  - A reset signal is implemented, allowing the controller to be reset to its initial state, which is useful during testing or in the event of a system malfunction.

## Implementation Details

### Finite State Machine (FSM)

The traffic light controller is designed using a Finite State Machine (FSM) approach, where each state corresponds to a specific traffic light configuration. The FSM transitions between states based on the clock signal and follows a predefined sequence to ensure that only one direction has a green light at any given time.

### Tools & Technologies

- **Language**: Verilog, a hardware description language.
- **IDE**: Xilinx Vivado
- **Concepts**: The design is grounded in the principles of Finite State Machines, which are crucial for implementing sequential logic and state transitions.

## Getting Started

### Prerequisites

To work with this project, you will need:
- Xilinx Vivado or any other compatible Verilog simulator.
- Basic understanding of Verilog and FSM design.

### Running the Simulation

1. Clone this repository to your local machine.
2. Open the project in Xilinx Vivado or your preferred Verilog IDE.
3. Synthesize the code to check for any design errors.
4. Simulate the code to observe the traffic light sequences and ensure correct operation.
5. Use the reset signal to test the controller’s ability to return to the initial state.
