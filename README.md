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

######Console logging
By default, the router sends all log messages to its console port. Hence only the users that are physically connected to the router console port can view these messages.
######Terminal logging
It is similar to console logging, but it displays log messages to the router's VTY lines instead. This is not enabled by default   
######Buffered logging
This type of logging uses router's RAM for storing log messages. buffer has a fixed size to ensure that the log will not deplete valuable system memory. The router accomplishes this by deleting old messages from the buffer as new messages are added.
######Syslog Server logging 
The router can use syslog to forward log messages to external syslog servers for storage. This type of logging is not enabled by default
######SNMP trap logging
The router is able to use SNMP traps to send log messages to an external SNMP server.
