# Linux Virtual Machine

If you're using a Linux Virtual Machine, you'll have fewer things to keep in mind compared to the Windows Subsystem for Linux setup.

1. Use your Linux Virtual Machine for pretty much everything that you do **except maybe video calls**.
2. Always assume your Linux Virtual Machine might disappear at any time without notice.

## Video calls might not work well

Sometimes, Virtual Machines don't play nicely with webcams. This might make video chatting from your Linux Virtual Machine environment difficult. The best way to work around this is to install and use your video chat software on your regular Windows 10 environment... and to do everything else \(coding, browsing the web, etc\) in your Linux Virtual Machine.

{% hint style="info" %}
Pro tip: If you're switching from your Linux Virtual Machine to your regular Windows 10 system often, you'll want to quickly figure out if it's possible to maintain a **shared clipboard** between the two environments. If this isn't working out in your favor, consider workarounds like installing Slack on both systems so you can send important notes to yourself.
{% endhint %}

## Don't _fully_ trust your Linux Virtual Machine

The Linux Virtual Machine is quick to setup, but it has its faults. Not only does it require the most amount of computer hardware resources out of all of the options we've laid out, but it's almost the most likely to fail on you.

Although rare, it's possible that your Linux Virtual Machine setup becomes corrupted. This is usually resolved by starting a new Linux Virtual Machine setup from scratch \(which you already know how to do\). **Unfortunately, this solution implies that all of your data on the corrupted Linux Virtual Machine setup is lost.** While this isn't too much of an issue if you're consistently pushing your work up to GitHub or backing up your files with Dropbox, you may be in a world of hurt otherwise.

{% hint style="warning" %}
Pro tip: Back up your work regularly if you're using the Linux Virtual Machine option.
{% endhint %}

