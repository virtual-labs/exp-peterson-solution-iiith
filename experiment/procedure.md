## Components of the Simulation

1. **Instructions Panel**

- Collapsible panel at the top of the simulation
- Contains step-by-step instructions for using the simulation
- Has an info button that provides additional context



2. **Controls Panel**

- Located on the left side of the simulation
- Contains Start/Pause and Reset buttons
- Displays the currently selected process
- Includes a legend explaining the color coding



3. **Simulation Area**

- The central component showing the visual representation of Peterson's algorithm
- Contains Process 0 and Process 1 representations
- Shows the turn variable and critical section
- Displays alerts when errors or violations occur



4. **Action Log**

- Located on the right side of the simulation
- Records all actions and state changes with timestamps
- Color-codes entries based on which process performed the action





## How to Use the Simulation

### Step 1: Start the Simulation

Click the **Start** button in the Controls panel to begin. This activates the simulation and allows interaction with the processes.

### Step 2: Select a Process

Click on either Process 0 (P0) or Process 1 (P1) to select it. The selected process will be highlighted with a ring around it, and the "Selected Process" indicator in the Controls panel will update.

### Step 3: Set the Process Flag

Click on the flag associated with the selected process to set it to true (T). This indicates that the process wants to enter the critical section. The process state will change from "inactive" to "active" (green).

### Step 4: Set the Turn Variable

Click on the turn variable to set it to the other process's number. This is part of Peterson's algorithm to ensure fairness.

- If Process 0 is selected, setting turn to 1 gives priority to Process 1
- If Process 1 is selected, setting turn to 0 gives priority to Process 0


### Step 5: Enter the Critical Section

Click the **Enter Critical Section** button below the selected process to attempt to enter the critical section. The algorithm will determine if the process can enter based on:

- If the process's flag is set to true
- If the other process's flag is false OR the turn variable is set to the selected process


If successful, the process will enter the critical section (red state), and the critical section area will show which process is currently inside.

### Step 6: Exit the Critical Section

When a process is in the critical section, click the **Exit Critical Section** button to make it leave. This will:

- Set the process state back to "inactive"
- Set its flag to false
- Update the critical section to show it's available


## Understanding the Color Coding

- **Gray**: Process is inactive
- **Green**: Process is active (flag is set, but not in or waiting for critical section)
- **Yellow**: Process is waiting to enter the critical section
- **Red**: Process is in the critical section


## Error Conditions

The simulation will display alerts in the following situations:

1. Attempting to enter the critical section without setting the process's flag
2. Attempting to enter when conditions aren't met (other process's flag is true and turn is set to other process)
3. Attempting to modify a flag while the process is in the critical section
4. Attempting to interact with the simulation before starting it
5. Attempting to enter the critical section with a process that isn't selected


## Observing the Algorithm

Watch the Action Log to see a detailed record of all operations. This helps understand the sequence of events and how Peterson's algorithm ensures mutual exclusion.

## Key Principles Demonstrated

1. **Mutual Exclusion**: No two processes can be in the critical section simultaneously
2. **Progress**: Processes outside the critical section cannot prevent other processes from entering
3. **Bounded Waiting**: No process can wait indefinitely to enter the critical section


By following these steps and observing the behavior, users can gain a practical understanding of how Peterson's Solution works to solve the mutual exclusion problem in concurrent programming.