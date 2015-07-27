sshplus
======

A custom version of ssh plus based on the original sshplus from Anil Gulecha.

Changes :

- Removed Launch text from indicator bar
- Fixed menu Refresh functionality
- Tested on Ubuntu 15.04

Configuration:
Create a file .sshplus in your home directory (touch ~/.sshplus).
Edit the file and add the entries in the format
NAME|COMMAND|arguments

For Example

```
# launcher applications
label:Quick Launch
folder:Applications
Show top|gnome-terminal|-x top
NASBox|nautilus|smb://192.168.0.99

# show a separator
sep

# ssh connections
label:SSH/SFTP Connections
RaspberryPi (SSH)|gnome-terminal|-x ssh pi@192.168.0.23
RaspberryPi (SFTP)|nautilus|sftp://pi@192.168.0.23

# show a separator
sep

# Settings
label:Settings
Edit Configuration|atom| /home/deepak/.sshplus
```

Install and Run:
git clone https://github.com/deepaksrivastav/sshplus.git
cd sshplus
chmod a+rx sshplus.py
sudo cp sshplus.py /usr/local/bin

To run:
/usr/local/bin/sshplus.py

Add this to the startup program list so that it runs when the user logs in.
