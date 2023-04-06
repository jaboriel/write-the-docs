---
layout: default
title: home
---

INSTALLING KVM HYPERVISOR ON MACOS

Homebrew Part

1.  Make sure that you have homebrew installed so that you can use the ‘brew’ package to install the necessary tools
2.  type ‘brew.sh’ in a web browser on your MAC computer and follow the instructions therein
    Homebrew is a tool that helps you install many linux based packages on MAC
3.  Install the QEMU stack on you MAC by typing in the terminal;
      brew install qemu
4.  Next install libvirt to control qemu stack use the command:
      brew install libvirt
5.  Start the VIRT server:
      brew services restart libvirt
6.  Install MAC PORT:
      Go to www.macports.org/install.php on a web browser
      Download the PORT software for your specific MAC OS version (pkg)
       Install it on your MAC (might require a reboot or close and reopen terminal to make the PORT command available)
Now move to the next part

Port Software Part

1.  On the new terminal install Virt-Manager
      sudo port install virt-manager
      For the “Continue” question, answer ‘Y’
      Virt-manager takes some time to fully install
2.  The last component is XQUARTZ for X11 systems, install it:
      Go to www.xquartz.org and download the PKG file and install it
      It will require you to log out of your system user at completion, Go ahead
3.  Now start virt-manager on the following command
      virt-manager -c qemu:///session --no-fork
      Wait for the Virtual Machine Manager to boot up
4.  Click on File and then New Virtual Machine
5.  If you have an ISO OS file on your Mac, Select Local Install media (ISO) click Forward
6.  Click on Browse and Browse Local and navigate to the location of the ISO disk (eg Ubuntu 18.04) on your computer
      Choose it and click Forward
