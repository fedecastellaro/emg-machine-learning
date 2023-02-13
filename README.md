# Platform for the Acquisition and Processing of Electromyographic Signals Oriented to Biomedical Applications. 

## Overview

Integral system designed to be able to capture any EMG signal produced by the body (in a non-invasive way) to be later translated by a previously trained neural network into an equivalent movement. 
The machine learning algorithm, the sampling of the analogue signals, and all the mathematical processing were all integrated in a 65x50mm PCB, making it 100% portable.

## PCB Design

It includes :
- WIFI/Bluetooth antenna for external connectivity
- Fully isolated USB connection
- 4 low noise differencial amplifiers
- Lithium-ion battery charger

## Software

This proyect includes three different king of software implementations:
- In C/C++ for the microcontroller.
- In Python for the PC.
- In Kotling for the Android App.

Briefly, the PCB acquires a one-second sample of the 4 signals while performing an action and stores it in a database.
Using the python program we can take all the saved samples and train our machine learning algorithm, which is then imported into the microcontroller.
The android application allows us to have full control of the actions performed by the PCB and displays the results of the machine learning algorithm.

## Improvements

- Replace the disposable electrodes with fixed ones.
- Implement a low-noise external ADC.
- GUI design for the PC program.
- Designing a pcb enclosure.
