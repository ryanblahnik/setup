# Windows 10 Users

Our curriculum, like the rest of the web development industry, is heavily dependent on open source software, which traditionally has not worked very well on Windows platforms. If you’re on a Windows machine, we’ve come up with a few solutions for you to put into place before the first day of class! If you’re already on a Unix-based system \(like macOS or Linux\), reading this section will not be a good use of your time.

## Recommended: Windows Subsystem for Linux

First, make sure you have the latest updates of Windows 10 installed. Our goal is to enable [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/faq) \(WSL\), also known as Ubuntu Bash for Windows 10. While the initial releases had some rough edges, the latest builds should work well enough for our curriculum.

Follow the setup instructions [here](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/). This option is our preferred option as you still get to use all of the applications you’re used to \(Sublime Text 3, Chrome, Zoom, etc\). However, _**all**_ of your terminal commands \(`git` commands, `node` commands, etc\) must be installed and run in Ubuntu Bash only and not via Windows 10’s PowerShell, Window 10’s Command Prompt, or via an `.exe` file in Windows 10. **If you choose this option, make sure you also setup the next option as a backup.**

## Backup: Virtual Machine

1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
2. Download and unzip the following pre-configured virtual disk image. If the unzip process fails, use [7zip](https://www.7-zip.org/) instead: [https://drive.google.com/open?id=1CopZmlURzq5ecKIMariQlW-3wsQOBlIv](https://drive.google.com/open?id=1CopZmlURzq5ecKIMariQlW-3wsQOBlIv%20)
3. Open the unzipped `.vbox` file with VirtualBox.

The image comes installed with:

* Node v6
* MySQL
* Sublime Text 3
* Git

## Alternative: Dual Boot Ubuntu and Windows 10

Run a Ubuntu dual-boot system. This is time intensive to setup, and should only be used as an option if you are unable to use the first two options. This means you have the option of booting your computer into Windows or Ubuntu \(but not both at the same time\) every time you turn it on.

[This document](https://docs.google.com/document/d/1jTk-tu1IeuztgLze8PFx5vRPVV-rwH8YqCC8hFT0VAM/) outlines the steps to set this up as well as notes from other instructors and students. Please feel free to add your own notes if you feel like they may help others in their own setup processes.



