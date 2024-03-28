# Process LinkedList Manager

The `process_linkedlist_manager.c` program is designed for managing a linked list of processes, where each process is represented as a node containing specific data attributes related to process management. This program is an enhanced version of a basic linked list input/output manager, tailored to handle process data efficiently.

## Data Structure

The program uses a custom data structure to represent each process:

```c
typedef struct process
{
  int pid;             // Process ID
  int priority;        // Process priority
  double processorTime;  // Time the process spends on the processor
} DATA_TYPE;

## Core Features

- **Appending Data**: Adds new process data to the end of the list.
- **List Traversal**: Prints the details of each process in the list.
- **File Input**: Loads process data from a specified file.
- **User Input**: Allows manual input of process data.
- **Data Allocation**: Dynamically allocates memory for process data.
- **Disk Output**: Saves the current list of processes to a file.
- **List Destruction**: Cleans up and frees allocated memory.

## Special Functionality

- **Move Last to First**: This feature rearranges the list by moving the last node to the front. It ensures that if the list is empty or has only one node, no action is taken. This function is crucial for scenarios where the most recently added process needs to be prioritized.

## Getting Started

### Compilation

To compile the program, use the following command:

```sh
gcc -o process_linkedlist_manager process_linkedlist_manager.c
