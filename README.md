# Platform for the Acquisition and Processing of Electromyographic Signals Oriented to Biomedical Applications. 

## Overview

Integral system designed to be able to capture any EMG signal produced by the body (in a non-invasive way) to be later translated by a previously trained neural network into an equivalent movement. 
The machine learning algorithm, the sampling of the analogue signals, and all the mathematical processing were all integrated in a 65x50mm PCB, making it 100% portable.

![alt text](https://github.com/fedecastellaro/emg-machine-learning/blob/main/Images/overview2.png?raw=true)

## PCB Design

It includes :
- WIFI/Bluetooth antenna for external connectivity
- Fully isolated USB connection
- 4 low noise differencial amplifiers
- Lithium-ion battery charger

![alt text](https://github.com/fedecastellaro/emg-machine-learning/blob/main/Images/PCB_R00.png?raw=true)

![Model](https://github.com/fedecastellaro/emg-machine-learning/blob/main/Images/overview.png?raw=true)


## Software

This proyect includes three different king of software implementations:
- In C/C++ for the microcontroller.
- In Python for the PC.
- In Kotling for the Android App.

Briefly, the PCB acquires a one-second sample of the 4 signals while performing an action and stores it in a database.
Using the python program we can take all the saved samples and train our machine learning algorithm, which is then imported into the microcontroller.
The android application allows us to have full control of the actions performed by the PCB and displays the results of the machine learning algorithm.

## Example of a sample of a one-second thumb movement

![Model](https://github.com/fedecastellaro/emg-machine-learning/blob/main/Images/data_raw.png?raw=true)

## Sample categorization of the ML classification algorithm by UMAP
Result of the dimensionality reduction technique called UMAP which allows us to observe how well the machine learning algorithm classifies each of the samples in the dataset.

Each color represented in the graph represents the samples of each classification group.

![alt text](https://github.com/fedecastellaro/emg-machine-learning/blob/main/Images/ML_%20UMAP.png?raw=true)


## Final Example

An example application is shown below, in which the PCB measures one second of the signal as the hand closes and is able to predict with 84% certainty the action in question.

![alt text](https://github.com/fedecastellaro/emg-machine-learning/blob/main/Images/final_grafico.png?raw=true?raw=true)


## Improvements

- Replace the disposable electrodes with fixed ones.
- Implement a low-noise external ADC.
- GUI design for the PC program.
- Designing a pcb enclosure.
