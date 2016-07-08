#Simple command to install password manager KeepassX version 2 on Debian 8 Jessie and Tails#

Debian Jessie stable and Linux distributions based upon it such as Tails, are currently using the old KeepassX version (0.4.3). 

This can be problematic when interacting other operating systems such as OSX, Windows and Ubuntu 16.04 are running the newer version of the app (2.0 and onwards) which introduce a new database format **(.kdbx)** that is not backward compatible with the old **(.kdb)** databases.

You can import the old **.kdb** databases into KeepassX 2.0 (and onwards) but you will then required to save the database in the new **.kdbx** format to access it. 

This command will install the newest version of KeepassX from the Debian Jessie backports repository. Make **absolutely sure** you have a backup of your password database before you attempt to migrate to the newer version of KeepassX.

###Launch the Terminal from the Applications Menu###

> Applications>Utilities>Terminal

![Launch Terminal](https://github.com/georgeowell/Install-KeepassX-V2-Debian-Jessie/blob/master/images/Launch%20Terminal.png)

###You can see the current available versions of KeepassX in Debian by running the command:###
```bash
apt list keepassx -a
```

###Running the command manually###

This command will require you to enter your root (sudo) password which you set at install on stock Debian or can optionally set at each boot of Tails by selecting "More Options" at the login menu.

```bash
sudo apt-get -t jessie-backports install keepassx
```

Then type in your root password and press enter.


###Running the command using the bash script
A bash script is a simple file which can simplify running complex commands.

You can copy the handy bash script `install-keepassx2` to your home directory `/home/yourusername/`. If you're using Tails with persistent storage, you should save to `/home/amnesia/Persistent/` to preserve the file between reboots.

You must then mark the script as an executable program to be able to run it:

Right click on the script and select Properties.

![Opening Properties](https://github.com/georgeowell/Install-KeepassX-V2-Debian-Jessie/blob/master/images/Opening%20Properties.png)

Then select the Permissions tab and tick the box that say "Allow executing file as program".

![Marking Bash Script As Executable](https://github.com/georgeowell/Install-KeepassX-V2-Debian-Jessie/blob/master/images/Marking%20Bash%20Script%20As%20Executable.png)

Then you can run the script by dragging it into the Terminal app and pressing enter. You should then be prompted to enter your root password. Hit enter and the script will run. You can then close the Terminal.


###Launch KeepassX###

You should now have version 2.02 of KeepassX installed. You can check this by launching KeepassX from the Applications menu.

> Applications>Accessories>KeepassX

Then select: 

> Help>About

![Find KeepassX Version Number](https://github.com/georgeowell/Install-KeepassX-V2-Debian-Jessie/blob/master/images/Find%20KeepassX%20Version%20Number.png)


###Any Problems?###
Open an issue on the project's Github page: [https://github.com/georgeowell/Install-KeepassX-V2-Debian-Jessie](https://github.com/georgeowell/Install-KeepassX-V2-Debian-Jessie)

Or try the Tails projects's help page: [https://tails.boum.org/support/index.en.html](https://tails.boum.org/support/index.en.html)
