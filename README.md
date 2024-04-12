# Command line tool for finding and pinging default gateway
This is the bash script I ever wrote. Since I am trying to land a support role and network troubleshooting is a big part of the, I decided to automate the process of finding the default gateways IP address and pinging it to see if it is up. I accomplished this by using the route command to pull up the routing table then grep for the line, and awk to pull the section that contains the IP we're looking for. I originally tried to use cut, but I was having issues with the delimiter.

## Prerequisites

- [Install WSL if you are on Windows. Skip if you are on Linux.](https://learn.microsoft.com/en-us/windows/wsl/install)

## How to setup

1. Place this script in ~/bin directory, where personal executable files such as scripts are intended to be stored.

## How to use

1. Type dgping in the shell.

## How it works

The script uses route -n to pull up the routing table then pipes it into grep, then pipes it into awk. We take the output and assign it to the variable "IP". It uses echo to display the IP of the defualt gateway to the screen, then pings the IP address four times.


## Contributing

Feel free to open up an issue or reach out to me.

 **Benjamin Zahirpour**
