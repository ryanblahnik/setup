# Windows Subsystem for Linux

Windows Subsystem for Linux \(WSL\) makes significantly easier for people who want to use and develop open source projects on Windows, but requires that you keep a few things in mind.

1. Understand the difference between installing/running applications on Linux Bash vs Windows 10.
2. Never modify any Linux files from a Windows 10 application.
3. To avoid huge wastes of time, don't modify the default shell that `Linux Bash` comes with to `zsh`, `fsh`, `ksh`, etc. \(If you don't know what this means, don't worry about it!\)

## Applications on Linux Bash vs Windows 10

At this point, you might already have Git and Node.js installed on your regular Windows 10 setup. While this works great for basic use cases, we'll want to use Linux Bash exclusively for command-line based applications \(like `git` and `node`\) because:

1. Linux Bash will have fewer problems running these applications \(more on that [here](https://docs.microsoft.com/en-us/windows/wsl/faq#why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows)\).
2. Having applications installed on both Linux Bash _**and**_ Windows 10 will be confusing and hard to keep updated.

### Install before Day 1

Here's a table that shows which software should be installed in which environments before W1D1:

| Application | Environment |
| :--- | :--- |
| [Sublime Text 3](https://www.sublimetext.com/3) | Windows 10 only |
| [Visual Studio Code](https://code.visualstudio.com/Download) | Windows 10 only |
| [Zoom](https://zoom.us/download#client_4meeting) | Windows 10 only |
| [Slack](https://slack.com/downloads/) \(note 1\) | Windows 10 only |
| Git \(note 2\) | Linux Bash only |
| Node.js via [nvm](https://github.com/creationix/nvm#install-script) \(note 3\) | Linux Bash only |

\(Note 1\) Students who don't install the standalone Slack desktop application usually have trouble keeping up with the course, so please make sure you install it.

\(Note 2\) Git should already be installed on Linux Bash. If you don't get an output for `git --version`, then run `sudo apt install git`.

\(Note 3\) One of the most reliable ways of install Node.js is via `nvm`, **not** via`apt install`. First, install `nvm` by running either of the [install scripts](https://github.com/creationix/nvm#install-script) via Linux Bash. Then, run `nvm install --lts` to install the latest "Long Term Stable" \(LTS\) version of Node.js, **not** the "Current" version of Node.js. You should now be able to run `which node`, which will indicate that your `node` command is installed in the `~/.nvm` directory.

### Install after Day 1

Below is a preview of some software that you may be installing and using after the first day of class. Don't bother looking into any of these things now, except to remove any previous installations of MySQL and MongoDB from your regular Windows 10 setup.

| Application | Notes | Environment |
| :--- | :--- | :--- |
| MySQL \(note 1\) | v5.7 \(not v8\) | Linux Bash only |
| MongoDB |  | Linux Bash only |
| [React](https://reactjs.org/) |  | via `npm` or `npx` only |
| [Webpack](https://webpack.js.org/) |  | via `npm` or `npx` only |
| [nodemon](https://github.com/remy/nodemon) |  | via `npm` or `npx` only |

\(note 1\) Some people may run into issues installing and running MySQL. In these cases, [installing the equivalent version of MariaDB instead](https://mariadb.com/kb/en/library/mariadb-vs-mysql-compatibility/#drop-in-replacement-for-mysql) is a great alternative.

## Never modify Linux files from Windows 10

This means that any files you want to open and modify with Windows 10 applications \(like Sublime Text, Visual Studio Code, Atom, etc\) need to already be located where Windows 10 already has access \(aka not in a secret Linux directory that is normally hidden from Windows 10\). When using WSL, a rule of thumb is: everything is a secret Linux directory **unless** it's in `/mnt/c`, which is where all of your Windows 10's `C:/` drive files are located. Here's an optional reading if you want to learn more:

{% embed url="https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/" caption="" %}

### How to modify Linux files

Given the above, how _**will**_ you modify important files stored in WSL's Linux-only directories then? The fastest way is to use a terminal-based text editor. While `vim` is often the default text editor \(that usually opens when you're trying to run `git log` or `git commit`\), it's not very beginner friendly. I recommend using `nano` instead.

So, when you need to tweak files like `.bash_profile` or `.bashrc` in your home directory, run `nano ~/.bash_profile` and peak at the hints on the bottom of your terminal to figure out how to exit and save \(or discard\) your edits.

### But where should you store your coding projects?

When you `git clone` your coding projects, you should put them in a place where your Windows 10 applications can see them as well. You can do this via Linux Bash by first running `cd /mnt/c` to change directory to your **C:/** drive. Continue to `cd` into wherever you normally store your coding projects, then `git clone` your project as you normally would.

