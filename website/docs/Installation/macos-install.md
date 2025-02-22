---
sidebar_position: 3
---

# MacOS

This page contains information regarding installation of Podman Desktop on MacOS. 

You can install Podman Desktop on Mac:
- Using the .dmg file, 
- Using Brew

If you don't have Podman installed, Podman Desktop will take care of installing it.

## Installing Podman Desktop on MacOS using .dmg file

1. Download the `.dmg` file from the [Downloads](/downloads/macos) section of this website.

While we recommend getting the "universal" binary file which will work irrespective of the chip architecture your Mac possesses, you also have the option to get the applicable .dmg file depending on your Mac Hardware Architecture (i.e. Intel or Apple M1).

2. Locate the downloaded file and and double-click on it. (Usually, you'll find the downloaded file under you Downloads folder)

> ![img0](img/download-dmg.png)

3. Drag Podman Desktop icon to the Applications folder.

> ![img1](img/click-and-drag.png)

4. Start Podman Desktop from the 'Launchpad' or Mac's 'Applications' directory.

> ![img2](img/podman-desktop-app.png)

5. Install Podman from Podman Desktop, if not yet installed. 

When you open Podman Desktop for the first time, click on the "View detection checks" button to scan if all the prerequisites to use Podman Desktop are met. If it says `❌ podman cli was not found in the PATH`, then you need to install the Podman CLI/Engine which can be done within the application. 

![img3](img/pd-before-podman.png)

- Click on the "Install" button next to the "View detection checks" button, and follow the instructions on screen. 
You will be redirected to the Podman Installer. Follow the instructions on screen and enter your system password when asked.

![img4](img/system-pass.png)

After installation is complete, close the installer.

6. You are ready to use Podman Desktop.

## Installing Podman Desktop on MacOS using [brew](https://brew.sh/).

### Prerequisites
- [Homebrew](https://brew.sh/)

### Installation steps

1. Open a terminal on your Mac.
2. Run the command below `brew install podman-desktop`.

Brew will also install the Podman CLI/Engine along with the Podman Desktop application, in case you don't have it installed yet. 

After the command is executed, you can find the Podman Desktop Application within the Applications directory of the MacOS.


## Next Steps

Learn more on how to get started with Podman Desktop by clicking [here](/docs/getting-started/getting-started).


