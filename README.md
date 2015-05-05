# About

This script will install Perforce Server 2015.1 on a 64-bit linux host. It has only been tested on Ubuntu so far. If you are looking for an Ubuntu host, I recommend the $20/month tier at [DigitalOcean](https://www.digitalocean.com/?refcode=070b959bc226).

# Usage

In shell, run the following commands in your terminal. You don't need to download this repo, that is what the first line in the following code does.

```shell
wget https://raw.githubusercontent.com/Allar/linux-perforce-installer/master/install-perforce
chmod +x install-perforce
sudo ./install-perforce
```

You will be asked to create a password and user details for a new unprivileged system user named `perforce`. You generally will never need to ever log into your server with this user, but I still suggest a password you won't lose. This is *not* a Perforce user, this is a Linux/Ubuntu user for the server only. You will create your Perforce user when you connect for the first time.

Afterwards, the server will restart and you should then be able to connect to your Perforce server.

# Security

The created server will have default Perforce installation settings. This means anyone who connects to your server can create a user account without authorization. After you create your first user, you should close this security hole by using the following `p4` command from your Perforce Client.

        p4 configure set dm.user.noautocreate=2
