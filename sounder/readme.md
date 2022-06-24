This project was made for the course ECE -GY - 6023 , Tandon School Of Engineeering ,NYU , 2022

#Measuring the channel frequency and time
response through simple channel sounding using
software defined radio.

#Software-defined radio (SDR) is a radio communication system where components that
have been traditionally implemented in hardware (e.g. mixers, filters, amplifiers,
modulators/demodulators, detectors, etc.) are instead implemented by means of
software on a personal computer or embedded system.While the concept of SDR is not
new, the rapidly evolving capabilities of digital electronics render practical many
processes which were once only theoretically possible.
A simple block diagram given below explains the main components and the flow of the
SDR.


#Setup
The setup for the receiver and sender modules were simply easy. The receiver and the
transmitter were attached to the same PC with maximum distance between them.
Attaching to the same PC allowed easy running of the scripts and avoided getting
irrelevant data if the receiver kept listening even if the sender stopped sending .


The actual interface to the PLUTO was done using the transmitter and receiver blocks
of the SDR in Simulink. The signal data was fed from the workspace of the Matlab to the
model in simulink. The received signal data was sent back to the workspace for the post
processing.
The figure below shows the Simulink block model of the transceiver system employed.
Since the transmitter block accepts a time series complex data , separate time series of
real and imaginary parts were imported into the model and then fed to the transmitter
block.

The receiver and the transmitter blocks are highly configurable. I used the following
parameters for the transmission and receiving.

#Center Frequency : 2.4 GHz
#Sample Rate : 1 MHz
#Samples per frame of the transmitter: 1024

These parameters are the same for the generated signals in the workspace. The model
will run the same time as the data and the receiver will receive the data at the same
sampling frequency and frame length
