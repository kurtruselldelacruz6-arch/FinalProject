# Page Replacement Simulator

## Project Overview

The Page Replacement Simulator is a C++ console-based project developed for the **Principles of Operating System** course at **National Teachers College

The program demonstrates how an operating system manages memory when the available memory frames are limited. It simulates three page replacement algorithms—First-In, First-Out (FIFO), Least Recently Used (LRU), and Optimal Page Replacement—and displays page hits, page faults, and the contents of memory frames after each page reference.

## Objectives

- Demonstrate the concept of page replacement in operating systems.
- Implement FIFO, LRU, and Optimal Page Replacement algorithms.
- Display memory frame changes, page hits, and page faults.
- Compare the results of the three algorithms using the same page reference string.

## Features

- Accepts a page reference string from the user.
- Allows the user to specify the number of page references and memory frames.
- Simulates FIFO, LRU, and Optimal Page Replacement.
- Shows the frame contents after each page reference.
- Identifies each reference as a **HIT** or **FAULT**.
- Displays the total number of page hits and page faults for each algorithm.
- Provides a menu to run one algorithm, run all algorithms, or exit.
- Checks several invalid inputs, including out-of-range reference/frame counts and negative page numbers.

## Algorithms Used

1. First-In, First-Out (FIFO)

FIFO replaces the page that has been in memory the longest. It follows the order in which pages entered the frames.

2. Least Recently Used (LRU)

LRU replaces the page that has not been used for the longest time.

3. Optimal Page Replacement

Optimal replaces the page whose next use is farthest in the future. If a page will not be used again, it can be selected for replacement. This algorithm is mainly useful for comparing results because it requires knowledge of future page references.

## Requirements

- A C++ compiler, such as `g++`
- A terminal or command prompt, or a C++ IDE such as Code::Blocks or Visual Studio Code with a configured compiler

## How to Compile and Run

1. Save the C++ source code in a file named `main.cpp` (or use the name of your source file).
2. Open a terminal in the folder containing the source file.
3. Compile the program:

   ```bash
   g++ main.cpp -o page_replacement
   ```

4. Run the program:

   **Windows:**
   ```bash
   page_replacement.exe
   ```

   **Linux/macOS:**
   ```bash
   ./page_replacement
   ```

If you are using an IDE, open the C++ source file, build the project, and run it using the IDE's controls.

## How to Use the Program

1. Enter the number of page references (**1–50**).
2. Enter the number of memory frames (**1–20**).
3. Enter the page reference numbers separated by spaces or new lines. Page numbers must be non-negative integers.
4. Choose an option from the main menu:
   `1` - Run FIFO
   `2` - Run LRU
   `3` - Run Optimal
   `4` - Run all three algorithms
   `5` - Exit
5. Review the frame contents, page hit/fault results, and totals displayed by the program.

## Sample Input

For example, you can enter:

```text
Enter number of page references (1-50): 5
Enter number of frames (1-20): 3
Enter the page reference string:
1 2 3 1 4
Enter choice: 4
```

The simulator will run FIFO, LRU, and Optimal using the same reference string and frame count. The exact page faults and hits depend on the selected algorithm.

## Understanding the Output

- Page: The page being requested.
- Frames: The pages currently stored in the available memory frames. A dash (`-`) represents an empty frame.
- HIT: The requested page is already in memory.
- FAULT: The requested page is not in memory and must be loaded; if all frames are occupied, a page may need to be replaced.
- Total Page Faults: The number of page references that caused a page fault.
- Total Page Hits: The number of page references that were already in memory.

## Testing

The project document reports tests for a reference string with three frames, repeated page references, zero page references, and zero frames. It reports that the test cases passed and that no major bugs or fixes were identified.

## Project Team

- Lloyd Vincent R. Halili
- Deiser Andrew M. Limpiado
- Gilbert Gabrielle G. Francisco
- Richmond Jay B. Bodino
- Andrey C. Francisco
- Kurt Rusell Dela Cruz

## Conclusion

This project demonstrates how page replacement supports operating-system memory management. By comparing FIFO, LRU, and Optimal Page Replacement, users can observe how different strategies handle the same page reference sequence and how they affect page hits and page faults.

---

Course: Principles of Operating System  
School: National Teachers College
