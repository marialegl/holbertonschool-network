## Networking basics #1

Learning Objectives

## localhost/127.0.0.1:

localhost is the domain name that refers to your own computer. It’s a way to access services or servers running locally.
127.0.0.1 is the IP address that represents localhost. It is a loopback address, meaning any traffic sent to this address stays on the same machine.

## 0.0.0.0:

0.0.0.0 is a special IP address that means "all addresses." It’s typically used to indicate that a server should listen on all available network interfaces on a machine.

## /etc/hosts:

This file is a static table that associates IP addresses with domain names. It’s a form of name resolution that occurs before querying DNS servers.

## Displaying Active Network Interfaces:

Network interfaces are the network connections your machine has. This can include physical interfaces like Ethernet or Wi-Fi, as well as virtual interfaces. You’ll need to know commands to list these interfaces and their statuses.

## Technical Requirements

1. Allowed Editors:

You can use vi, vim, or emacs to write your scripts or edit files.

2. Operating System:

All work must be compatible with and tested on Ubuntu 20.04 LTS.

3. File Ending:

All files must end with a new line.

4. README.md:

You must create a README.md file at the root of your project that explains what the project does and how to use it.

5. Bash Scripts:

All your scripts must be executable and written in Bash.
- Scripts must pass the Shellcheck tool (version 0.7.0) without errors.
- The first line of each script should be #!/usr/bin/env bash to ensure it runs in the correct Bash environment.
- The second line should be a comment explaining what the script does.


## Important Commands

1. ifconfig:

Command to display active network interfaces and associated configurations.

2. telnet:

Used to manually establish network connections, such as checking if a specific port on a remote server is open.

3. nc (Netcat):

A versatile tool for working with networks. It can act as a client or server and allows you to send and receive data over the network.

4. cut:

Used to cut sections from each line of a file or input.


## Steps to Follow

1. Read the Resources:

Familiarize yourself with the concepts mentioned in the recommended resources.

2. Create Scripts:

Create Bash scripts that implement the assigned tasks, ensuring you meet the formatting and compatibility requirements.

3. Testing:

Run and test your scripts in an Ubuntu 20.04 LTS environment to ensure they work correctly.

4. Documentation:

Document your project in the README.md file, detailing how the scripts should be executed and what results to expect.


This project will help you build a solid foundation in understanding and managing networks in Linux-based systems, which is crucial for administering servers and development environments.