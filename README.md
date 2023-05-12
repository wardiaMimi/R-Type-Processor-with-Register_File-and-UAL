# R-Type-Processor-with-Register_File-and-UAL
This is a 16-bit R-type instruction processor with register file, UAL, and instruction memory (RAM). Ideal for learning about processor design, it supports 8 arithmetic and logic operations and provides a starting point for building more complex designs.
# Getting started 
To get started with this project, you'll need to have Logisim installed on your computer. Logisim is a free and open-source tool for designing and simulating digital circuits.
1.  Download the Logisim file, main.circ, to your local machine.
2.  Open Logisim and click "File" > "Open" to open the main.circ file.
3.  You should now see the processor design in Logisim. You can interact with the processor by clicking on the various components, such as the registers and the UAL, and editing their properties.
## Usage
#### The instruction format for this project consists of 16 bits divided into 5 parts:
Bit 0 | Bits 1-3 | Bits 4-7 | Bits 8-11 | Bits 12-15 
--- | --- | --- | --- |--- 
Stop bit | operation code | Destination register |  operand 1 |  operand 2

The available operation codes are:

    op = 000 : add
    op = 001 : sous
    op = 010 : mul
    op = 011 : AND
    op = 100 : OR
    op = 101 : XOR
    op = 110 : NOT

- To enter your own instructions, there are two options. 
The first option is to set the "active" bit to 1 and then start writing in the "inst_in" field with the corresponding "inst_adr" address. Click on the clock of the instruction memory ``` clk_int``` to create a rising edge to store the instruction.


![image](https://github.com/wardiaMimi/R-Type-Processor-with-Register_File-and-UAL/assets/91344458/0735268c-3b6f-4c9b-b8ad-5a7bb0939161)

Alternatively, you can directly click on the field where you want to write your instruction. When the borders are red, you can start writing in hexadecimal format.

![image](https://github.com/wardiaMimi/R-Type-Processor-with-Register_File-and-UAL/assets/91344458/43e557d7-4ac8-493a-a798-2955472ec82c)

##### For example
the instruction ```add r0, r1, r2``` would be represented as ```0000 0000 0001 0010``` in binary or ```0012``` in hexadecimal.

- To finish your program, you need to include the instruction ```9000``` to stop the PC.

- To fill the registers in the register file, set the "active" bit to 1 and then fill the "A_in" field with the register address (0000 to 1111) and the "D_in" field with the corresponding data (number). Click on the clock of the register file ```clk_reg``` to create a rising edge to store the instruction.
#### After initializing the register file and the instruction memory
- set "active" to 0 and make sure the PC is set to 0. You can clear the PC by putting this bit to 1.

#### To start the simulation, click  "simulate" > "ticks enabled" or click ```ctrl + k```
- As the simulation begins, the clock will switch between high and low states, causing the program counter to increment and the program to begin execution.

- You can verify the results in the destination registers in the register file.

[processor.webm](https://github.com/wardiaMimi/R-Type-Processor-with-Register_File-and-UAL/assets/91344458/001b0b36-8a6e-48f2-b8d4-e26812aad265)

## Contributing
Thank you for your interest in contributing to this project! Here are the steps to follow to make changes and submit a pull request:
Fork the repository by clicking the "Fork" button on the GitHub page.

  - Download the Logisim file, main.circ, to your local machine.

  - Make your changes to the Logisim file.

  - Commit your changes with a brief description of what you changed.

  - Push your changes to your forked repository.

  - Submit a pull request by clicking the "New Pull Request" button on the GitHub page.

  - Provide a brief description of your changes in the pull request message.

  - Wait for the project owner to review your changes and provide feedback.

  - Once your changes have been approved, the project owner will merge them into the main repository.

If you have any questions or need help with the contribution process, please don't hesitate to contact us by creating an issue in the GitHub repository.

We welcome all contributions, no matter how small or large, and we appreciate your help in making this project even better! 
