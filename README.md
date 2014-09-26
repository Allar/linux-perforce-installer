# About

This script will install Perforce Server 2014.1 on a 64-bit linux host. It has only been tested on Ubuntu so far.

# Usage

In shell, run the following commands:

```shell
wget https://raw.githubusercontent.com/Allar/linux-perforce-installer/master/install-perforce
chmod +x install-perforce
sudo ./install-perforce
```

You will be asked to create a password and user details for a new user named `perforce`.

Afterwards, the server will restart and you should then be able to connect to your Perforce server.
