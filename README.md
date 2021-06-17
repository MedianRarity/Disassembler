<!-----------------------------------------------------------------
 Project:  Programming Assignment 1 - SIC-XE-Disassembler
 File: README.md
 Notes:    Program takes two inputs, .obj file and .sym file (IN THAT ORDER),  and converts it into one output, an .lis file.
                All input/output files are in .txt format for convenience.
--------------------------------------------------------------------->

## SIC-XE-Disassembler



#### The Program:
    Opens an SIC/XE object file, and its accompanying symbol file.
    Then it will disassemble the object code, and generate an sample.lis file.

#### The Algorithm:

    This program stores the content of the .obj and .sym files in three separate 2D vectors,
    objectCode, symCode, and literalCode. These 2D vectors are passed to the writeLis() function.
    The function works with the object vector to perform every calculation of the object code in a
    while loop, while also checking if any symbols or literals need to be included. The function
    also writes the output lis file while it is performing the calculations, uses several helper
    functions, and uses a struct containing every opcode with its respective mneumonic and format.

    

**For a2 directory (EDORAS):**

    In order to check the program in edoras you can use the username: cssc2827 and password: CjC/3D/5
    There is an a2 directory with all the required files. Next, you can follow the "Make Instruction"

#### Files Included:
**README.md**:

    A README file describing the program and detailing its files.

**main.cpp**:

    The file cointains an algorithm that opens an SIC/XE object file and its accompanying symbol file, which then disassembles the object code, and generate an SIC/XE source file, and SIC/XE listing file using the assembled code.

**main.hpp**:

    Declares and briefly explains functions implemented in main.cpp.

**Makefile**:

    Creates a compiled version of main.cpp.

#### Compilation Instructions:



**Make Instructions:**

    make all:
    	compiles the main file

    make clean:
    	deletes the main file, and the <filename>.lis file


**Running the Program:**
    
    type "make" the Makefile should do everything for you


#### Operating Instructions:
**Required Input**:

    The input filename needs to be the filename that has a sample.obj and a sample.sym file extension.
        The sample.obj file needs to be an object file of SIC/XE machine.
        The sample.sym file needs to be a symtab and littab file for the SIC/XE machine.

#### Significant Design Decisions:
    The data from the sample.sym file is stored in a linked list.
    We store interpreted text records inside a vector while we are reading the object file.

#### Extra features:

    Makefile also cleans excutable file and sample.lis in addition to the required main.

<!-----------------------------------------[ EOF: README.md ]--------------------------------->
