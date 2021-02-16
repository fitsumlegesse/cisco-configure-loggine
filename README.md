# CISCO-Configure-Logging 

 Logging can use for fault notification, network forensics, and security auditing.
 Cisco routers log messages can handle in five different ways:
 >Console logging
 >
 >Terminal logging
 >
 >Buffered logging
 >
 >Syslog Server logging
 >
 >SNMP trap logging

### Console logging
By default, the router sends all log messages to its console port. Hence only the users that are physically connected to the router console port can view these messages.
### Terminal logging
It is similar to console logging, but it displays log messages to the router's VTY lines instead. This is not enabled by default   
### Buffered logging
This type of logging uses router's RAM for storing log messages. buffer has a fixed size to ensure that the log will not deplete valuable system memory. The router accomplishes this by deleting old messages from the buffer as new messages are added.
### Syslog Server logging 
The router can use syslog to forward log messages to external syslog servers for storage. This type of logging is not enabled by default
### SNMP trap logging
The router is able to use SNMP traps to send log messages to an external SNMP server.

### Level name

### Router messages

0	Emergencies	System shutting down due to missing fan tray <br/>
1	Alerts	Temperature limit exceeded <br/>
2	Critical	Memory allocation failures <br/>
3	Errors	Interface Up/Down messages <br/>
4	Warnings	Configuration file written to server, via SNMP request <br/>
5	Notifications	Line protocol Up/Down <br/>
6	Information	Access-list violation logging <br/>
7	Debugging	Debug messages <br/>


### Buffered Logging 
To use logging buffered configuration command to enable the local storage of router log messages: <br/>

Router#configure terminal <br/>
Enter configuration commands, one per line.  End with CNTL/Z. <br/>
Router(config)#logging buffered informational <br/>
Router(config)#end <br/>

You can also Set the Log Size on router.<br/>
Router#configure terminal<br/>
Enter configuration commands, one per line.  End with CNTL/Z.<br/>
Router(config)#logging buffered 64000 <br/>
Router(config)#end <br/>

###### Terminal Logging 
Use the terminal monitor command to enable the displaying of log messages to your VTY: <br/>

>Router#terminal monitor <br/>
>
>Router# <br/>

To disable logging to your VTY session, use the following command: <br/>

>Router#terminal no monitor <br/>
>
>Router# <br/>


### Syslog  Server Logging 
If you have any syslog server please find the below simple config. <br/>

>router#conf t <br/>
>
>Router(config#logging host x.x.x.x <br/>
>
>Router(config)#logging traps (i.e 0 1 2 3 4 5 .. according to your requirement) <br/>

before enabling logging be sure that your router is properly configure to collect proper time from any NTP server or manually configure to get time <br/>
>Command to set time manually on router is 
>(set clock) 
to use ntp server use 
> “ntp server x.x.x.x” to sync clock to router.

### Clearing the Router's Log

Use the clear logging command to clear the router's internal log buffer:

>Router#clear logging
>
>Clear logging buffer [confirm]<enter>
>Router#
 
### To display the state of system logging 
use the show logging privileged EXEC command.
 >Router# show logging



