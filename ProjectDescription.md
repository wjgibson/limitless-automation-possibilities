# Project Description

## Summary

The visual IDE for lap will be used by automation engineers to write programs to write automation software in a quick, and simplistic manner. Thanks to the ease of use of this software, minimal training will be needed for engineers to begin writing code that can be used in production. In this program, users will have a list of instructions and steps that can be dragged onto a development pane as a node. These nodes will be able to be connected with lines and exported to a program that can be executed using the step by step instructions that the developer wrote. This visual style of programming makes automation engineering much more accesible to new users, helping new clients to be interested in LAP 

## High-level Features

<ul>
  <li>[UC1] Create nodes that contains a step for a machine.</li>
  <li>[UC2] Connect existing nodes together to make a series of steps.</li>
  <li>[UC3] Add a configuration to the system.</li>
  <li>[UC4] Remove nodes from the configuration.</li>
  <li>[UC5] Save a configuration to the database.</li>
  <li>[UC6] Load a configuration from the database.</li>
</ul>

## Non-Functional Requirements

  <ul>
    <li>[NR1] The system shall load the instructions dynamically and quickly from the database.</li>
    <li>[NR2] The configuration pane should be responsive and intuitive to use.</li>
 </ul>

## Constraints

<ul>
  <li>MSSQL must be used as a database.</li>
  <li>There should be no code required for the user to use this software.</li>
</ul>
