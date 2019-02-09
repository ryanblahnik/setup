# Windows 10 Users

Our curriculum, like the rest of the web development industry, is heavily dependent on open source software, which traditionally has not worked very well on Windows platforms. If you’re on a Windows machine, we’ve come up with a few solutions for you to put into place before the first day of class! If you’re already on a Unix-based system \(like macOS or Linux\), reading this section will not be a good use of your time.

## Recommended: Windows Subsystem for Linux

First, make sure you have the latest updates of Windows 10 installed. Our goal is to enable [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/faq) \(WSL\), which gives us access to Linux Bash for Windows 10. While the initial releases had some rough edges, the latest builds should work well enough for our curriculum.

Follow the setup instructions [here](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/). This option is our preferred option as you still get to use all of the applications you’re used to \(Sublime Text 3, Chrome, Zoom, etc\). However, _**all**_ of your terminal commands \(`git` commands, `node` commands, etc\) must be installed and run in Linux Bash only and not via Windows 10’s PowerShell, Window 10’s Command Prompt, or via an `.exe` file in Windows 10. **If you choose this option, make sure you also setup the next option as a backup.**

Be sure to read more about how you should use Windows Subsystem for Linux [here](windows-subsystem-for-linux.md).

## Backup: Linux Virtual Machine

Setting up a Linux Virtual Machine as a backup option is a fairly painless process if your computer has enough hard drive space, CPU, and RAM to handle it. The best way to find out is to give it a whirl, and see your system handles the Virtual Machine.

1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
2. Download and unzip the following pre-configured virtual disk image. If the unzip process fails, use [7zip](https://www.7-zip.org/) instead: [https://drive.google.com/open?id=1ZpE-tGDDQF8LLZUL4he6gy0J54HcTn5Z](https://drive.google.com/open?id=1ZpE-tGDDQF8LLZUL4he6gy0J54HcTn5Z)
3. Open the unzipped `.vbox` file with VirtualBox.
4. You may find it useful to change the Display Settings inside your Virtual Machine to match your screen resolution.
5. Make sure you configure Git with your [name](https://help.github.com/articles/setting-your-username-in-git/) and the [email address you use for GitHub](https://help.github.com/articles/setting-your-commit-email-address-in-git/)!

The image comes installed with:

* Ubuntu 18.04
* Sublime Text 3
* Visual Studio Code
* Google Chrome
* Slack
* Git
* Node 10
* MariaDB \(direct replacement for MySQL\)

Be sure to read more about how you should use your Linux Virtual Machine [here](linux-virtual-machine.md).

## Alternative: Linux Dual Boot

Setup a Ubuntu dual-boot system. This is time intensive to configure, and should only be used as an option if you are unable to use the first two options. This means you have the option of booting your computer into Windows or Ubuntu \(but not both at the same time\) every time you turn it on.

[This document](https://docs.google.com/document/d/1jTk-tu1IeuztgLze8PFx5vRPVV-rwH8YqCC8hFT0VAM/) outlines the steps to set this up as well as notes from other instructors and students. Please feel free to add your own notes if you feel like they may help others in their own setup processes.

Be sure to read more about how you should use your Linux Dual Boot system [here](linux-dual-boot.md).

