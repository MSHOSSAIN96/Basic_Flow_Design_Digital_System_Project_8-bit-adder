# Basic Flow Design Digital System Project 8-bit-adder
A design flow for creating an IC named 8-bit adder with registered inputs and outputs. 


**Chapter 1 Simple Basic Design flow**

This directory aims to describe the design flow for creating an IC. The module that I am going to develop as an example is an 8-bit adder with registered inputs and outputs; it is called **my_adder**.

**1.1 Goals:**

In this repository, the design flow that I am going to perform includes the following steps:

1.RTL design and simulation

2.Synthesis of the RTL code to produce a netlist

3.Simulation of the gate-level netlist with back-annotated delays

4.Place and Route of the design to produce a layout


The general view of the flow is shown in the following picture:


![Screenshot 2024-12-15 125446](https://github.com/user-attachments/assets/f35c7811-6e60-448c-9753-b6c483836b81)



**1.2 Organise your data**

Before start with the design flow, it is a good idea to create a set of directories where I will put the data generated during the design flow. All the files in the design are located in the directory **my_adder**. 

Inside this directory, I need the following subdirectories:

rtl: This sub-directory will contain the VHDL files that model design. The files are at the Register-Transfer-Level (RTL).

tb: This sub-directory will contain the VHDL files that I need for the simulation of the design. They define the test-bench. Note that they are not going to be synthesised.

gate: This sub-directory will contain the gate-level netlist that results out of the synthesis.

layout: This sub-directory will contain the layout of the design after the place and route process.

Open a new terminal and go to the directory where I want to work. In that terminal, I can create the required directories executing with the following shell commands:

**mkdir my_adder

mkdir my_adder/rtl

mkdir my_adder/tb

mkdir my_adder/gate

mkdir my_adder/layout**

It is also a good idea to create a new sub-directory for each tool that I want to use. They are:

**do_sim: A sub-directory for running the simulation (at the RTL and at the gate level).

do_synth: A sub-directory for running the synthesis.

do_pr: A sub-directory for running the place and route.

mkdir my_adder/do_sim

mkdir my_adder/do_synth

mkdir my_adder/do_pr**

Now that I have a clear structure for my data, I can start with the implementation.
