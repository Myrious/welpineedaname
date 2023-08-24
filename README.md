# welpineedaname
I made this to bypass website blocking on the school computers.
In theory it should work because firefox can run on the chromebooks, but the download is blocked. Github, however, isn't. Installing Firefox on Chromebook seems to be rather difficult however so I have included the mozilla article about how to do it.
Run Firefox on ChromeOS
Firefox can now be installed on Chromebooks and other devices running ChromeOS. This article will explain the system requirements needed in order to run Firefox on ChromeOS and how to set this up.

How to run Firefox on ChromeOS
To run Firefox on ChromeOS, you first need to ensure that your system meets the following requirements:

System Requirements
x86 based Chromebook running ChromeOS 80 or later
You can check this by going to chrome://version in the Chrome browser address bar. Follow these instructions from Google if you need to upgrade your OS.

Enable Linux support for ChromeOS
Click here to learn more about how to set up Linux (Beta) on your Chromebook: https://support.google.com/chromebook/answer/9145439

Once you've enabled Linux, check the Terminal to see if you have the correct version:

cat /etc/os-release

If the version is not 10 (buster) or above, you'll need to run the update script:

sudo bash /opt/google/cros-containers/bin/upgrade_container

This script will take some time depending on how fast your Chromebook and internet speeds are. Once it's done, you'll need to restart your Linux container. You can either right click the Terminal icon and select Shut down Linux (Beta) or just restart your Chromebook.

Enable Flatpak
Flatpak is a new packaging format for Linux, click here to learn how to add Flatpak support:
Chrome OS Quick Setup
Follow these simple steps to start using Flatpak

Flatpak applications can be installed on ChromeOS with the Crostini Linux compatibility layer. This is not available for all ChromeOS devices, so you should ensure your device is compatible before proceeding. A list of compatible devices is maintained here.

Enable Linux support
Navigate to chrome://os-settings, and scroll down to Developers and turn on Linux development environment. ChromeOS will take some time downloading and installing Linux.

Start a Linux terminal
Press the Search/Launcher key, type "Terminal", and launch the Terminal app.

Install Flatpak
To install Flatpak, run the following in the terminal:


       sudo apt install flatpak
    
A more up to date flatpak package is available in the Debian backports repository.

Add the Flathub repository
Flathub is the best place to get Flatpak apps. To enable it, run:


       flatpak --user remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
    
Restart
To complete setup, restart Linux. You can do this by right-clicking terminal, and then clicking "Shut down Linux". Now all you have to do is install some apps!

Install Firefox
Once the setup is complete, you can install Firefox from a Terminal:

flatpak install firefox
