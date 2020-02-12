# reach-sio-agent
Reach Serial IO Agent
Serial to QML Communication
In order for your microcontroller to communicate with the QML Viewer
(a tool for loading QML documents that makes it easy to quickly develop and debug QML applications) 
messages being sent need to be translated. 
We have created a set of tools called the Serial Input/Output Agent (SIO) and
Translator Input Ouput Agent (TIO) agents to make this translation happen.

# SIO Agent
SIO Agent stands for Serial Input/Output Agent.
It is a program that runs in the background and handles serial communication for the Display Module. 
The SIO Agent passes its output to the TIO Agent which translates the messages into a form that the QML Viewer can understand.