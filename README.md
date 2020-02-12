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

#Technical Details
The SIO Agent is installed to /application/bin/sio-agent on the root file system. The agent is started by the init system which executes the /etc/init.d/sio-agent script on start up.

The SIO Agent excepts the following command-line options:

-b or –baud= – Sets the baud rate used on the serial port. The default is 115200 (8 bits, no parity, one stop bit). The supported baud rates are 115200, 57600, 38400, 19200, 9600 and 1200.

-d or –daemon – Runs the sio-agent in the background.

-e or –test – Used for testing.

-i or –stdio – Uses standard I/O instead of serial port.  Mostly used for host development.

-o or –logfile= – Logs to a file instead of standard error.

-p or –pty – Uses a pseudo terminal instead of serial port. Mostly used for host development.

-s[]or –sio_port[=] – Uses a TCP socket instead of domain socket. Default port is 7880.

-t []or –serial [] – Uses the device . The default is /dev/ttyUSB0.

-v or –verbose – Prints debug messages.

-h or –help – Prints usage information.

The startup script can also accept the following commands:

start

restart

stop
