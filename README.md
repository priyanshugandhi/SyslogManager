# SyslogManager
Syslog is a way for network devices to send event messages to a logging server – usually known as a Syslog server. The Syslog protocol is supported by a wide range of devices and can be used to log different types of events. The Assignment is to collect Syslog from any syslog source, retrieve the Events from the Syslog &amp; display the events.

Syslog is a standard for computer message logging. It permits the separation of software that generates the messages from the system that stores them and the software that reports and analyzes them.

Syslog can be used for computer system management and security auditing as well as generalized, informational and debugging messages. It is supported by a variety of devices and recievers across multiple platforms. Because of this syslog can be used to integrate log data from different types of systems into a central repository.


![alt text](https://www.logzilla.net/assets/images/blog/post_images/syslog-essentials/syslog-severities.png)

## Setting up the Development Environment

First make sure that you have rsyslog already installed on your system.

Rsyslog is a rocket-fast system for log processing.

It offers high-performance, great security features and a modular design. While it started as a regular syslogd, rsyslog has evolved into a kind of swiss army knife of logging, being able to accept inputs from a wide variety of sources, transform them, and output to the results to diverse destinations.

They are available for:

 * RPM-based systems: https://www.rsyslog.com/rhelcentos-rpms/
 * Ubuntu: https://www.rsyslog.com/ubuntu-repository/
 * Debian: https://www.rsyslog.com/debian-repository/
 
 Then we need to configure the `rsyslog.conf` file. In ubuntu this file can be located under /etc/ directory. Specify the ruleset and provide the TCP syslog reception.
 
 ![alt text](https://www.logzilla.net/assets/images/blog/post_images/syslog-essentials/syslog-severities.png)
 
 
Now move to the /var/log/ directory and type the following commands inside the terminal:

```
sudo service rsyslog restart
```
```
tail syslog
```

We can notice different syslog event along with its severity. 


## Future Integration

We can then integrate the backend using Python, Flask and Sqlite to retrieve the events and hence design a web based GUI for the Syslog Manager with following menu options.

Acknowledge – the Acknowledgement state (Acknowledged/Unacknowledged) of the
event should be changed through this menu option
Delete – This option should perform deletion of the event
Properties – This option should display the properties of the event
