# Cisco Cheatsheet | Packet Tracer

## Cisco IOS (Interface Operating System)
### In wikipedia
> The IOS command line interface provides a fixed set of multiple-word commands. The set available is determined by the "mode" and the   privilege level of the current user. "Global configuration mode" provides commands to change the system's configuration, and "interface  configuration mode" provides commands to change the configuration of a specific interface. All commands are assigned a privilege level,  from 0 to 15, and can only be accessed by users with the necessary privilege. Through the CLI, the commands available to each privilege  level can be defined.
### Interfaces

- User EXEC Mode
- Privileged EXEC Mode
- Global Configuration Mode
- ROM Monitor Mode
- Setup Mode
- More than 100 configuration modes and submodes.

## Commands

### PC Configuration
#### IP Configuration
- IP
- Subnet Mask
- Default Gateway

### Router, Switch Configuration

### Hostname
```
hostname this_is_the_name
```
### Passwords

#### User EXEC Mode Password
```
Router2> enable
Router2# configure terminal
Router2(config)# enable secret mysecretpassword
```

#### Privileged EXEC Mode Password
```
Router2> enable
Router2# configure terminal
Router2(config)# enable password mypassword
```

#### Minimum Password Lenght
```
security passwords min-length 8
```

#### Max Log In Attempts
```
switch# login block-for 3 attempts tries within 30
```
#### Session Timeout
```
switch# terminal session-timeout 10
```

#### Configure Passwords on the Line
##### There are four main types of TTY lines
> The CTY line-type is the Console Port. On any router, it appears in the router configuration as line con 0 and in the output of the 
> show line command as cty. The console port is mainly used for local system access using a console terminal.

> The TTY lines are asynchronous lines used for inbound or outbound modem and terminal connections and can be seen in a router or access > server configuration as line x. The specific line numbers are a function of the hardware built into or installed on the router or 
> access server.

> The AUX line is the Auxiliary port, seen in the configuration as line aux 0.

> The VTY lines are the Virtual Terminal lines of the router, used solely to control inbound Telnet connections. They are virtual, in 
> the sense that they are a function of software - there is no hardware associated with them. They appear in the configuration as line 
> vty 0 4.

#### Configuration Procedure

1. From the privileged EXEC (or "enable") prompt, enter configuration mode and then switch to line configuration mode using the following commands. Notice that the prompt changes to reflect the current mode. 
```
router# configure terminal
Enter configuration commands, one per line.  End with CNTL/Z.
router(config)# line con 0
router(config-line)#
```
2. Configure the password, and enable password checking at login.
```
router(config-line)# password letmein
router(config-line)# login
```
3. Exit configuration mode.
```
router(config-line)# end
router#
%SYS-5-CONFIG_I: Configured from console by console
```
## SSH Connections

### Local User
### No Telnet
### Configure IP interfaces and Descriptions
### crypto key generator
### ip domain-name stya.lab
