# hyperion
# Project Sentinel: Intelligence Layer Prototype

## Overview
This project is an experiment to build a simple AI in C#. 
The goal is to create a system that doesn't just run a script once, but actively monitors provided data, 'thinks', and makes decisions on its own.

1.  **System awareness:** Watching the environment (Inputs).
2.  **Reasoning:** Analyzing changes in state (Logic).
3.  **Action:** Executing commands based on decisions (Outputs).

## Technology
* **Language:** C# (.NET 8)
* **Type:** Console Application (Modular architecture)

---

## Plan

**Current status:** Planning

### Phase 1: The core structure
*Focus: Getting the main loop running.*

* [ ] **Create the project:** Set up a C# Console Application.
* [ ] **The loop":** Write a `while(true)` kinda loop. The program should not stop, it needs to keep running to monitor the "environment".
* [ ] **Basic interfaces:** Create simple parent classes for `Sensor` (Input) and `Action` (Output).
    * *Note: I have to make sure new sensors can be added easily later.*

### Phase 2: Making "Sensors" 
*Focus: Giving the AI some data to look at.*

* [ ] **Mock data:** Since i don't have real hardware sensors yet, i will create classes that generate fake numbers (Random):
    * `TempSensor`: Simulates CPU temperature.
    * `UsageSensor`: Simulates RAM usage.
* [ ] **Reading data:** Make the main loop print these numbers to the console every second.

### Phase 3: The "Brain" 
*Focus: Making the system decide things by itself.*

* [ ] **Logic class:** Create a class that takes the sensor numbers and checks them.
* [ ] **Rules:**
    * If temp > 90 -> Danger.
    * If temp < 40 -> Ok.
* [ ] **Memory (optional):** Try to make it remember the previous state (so it doesn't panic if the temp spikes for just 1 second).
