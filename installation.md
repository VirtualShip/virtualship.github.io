---
layout: default
title: Installation
nav_order: 2
---

# Installation Guide
{: .fs-9 }

Learn how to install VirtualShip the quick and the slow way.
{: .fs-6 .fw-300 }


# For Mac OS
The preferred method to install VirtualShip on Mac OS is using the script method. However, it is till in its alpha stages, so if this method doesn't work, try manually installing it. Here is an overview of what the script does:
* Installs dependencies
* Installs VirtualShip

You may notice that we make use of HomeBrew, another package installer, to install these dependencies. In the future, we may release a major release to remove the python and gdown dependencies (see News for more info). Alright, so simply type the following code into the terminal to install:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/VirtualShip/Core/main/.install)"
```
And you're done!

## Create Folders
The next step is to create the folders, in which VirtualShip will operate in. We will need to create two folders: ```Warehouse``` and ```Garage```. All three of these folders will be created in the ```/usr/local``` directory.
### Warehouse
First, we need to create the Warehouse location. Navigate to ```/usr/local`` with the following:
```
cd /usr/local
```
Next, we will need to create the Warehouse folder. The Warehouse folder is the location where all the code in this repository is stored, so we will create this folder first. Run the following (it will ask for a password):
```
sudo mkdir Warehouse
```
Note: the below folder commands assume you stay in the ```/usr/local``` directory.
### Garage
The Garage folder is where VirtualShip will store the actual package you want to download. Do the same thing that we did for Warehouse:
```
sudo mkdir Garage
```
### Permissions
And all the folders should be created now. The next step is to modify the permissions of these three folders using the ```chmod``` command. Run the following commands below (it may ask for your password):
```
sudo chmod -R 777 Warehouse
sudo chmod -R 777 Garage
```
Note: The above commands assume you are in the directory ```/usr/local```

## Edit PATH
After you create all of these folders, you must update the PATH variable to match. The PATH is what the system looks for when you run a command. If these folders are not in the PATH variable, the shell will return a ```command not found``` error, which no one wants. We will need to add:
```
/usr/local/Warehouse
/usr/local/Warehouse/bin
/usr/local/Garage
/usr/local/Garage/bin
```
to the path. In order to do this, we must run the following command:
```
export PATH="/usr/local/Warehouse:/usr/local/Warehouse/bin:/usr/local/Garage:/usr/local/Garage/bin:$PATH"
```
And it should work. To check if it updated correctly, run this command:
```
echo $PATH
```
It should return something like the following:
```
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/Warehouse:/usr/local/Warehouse/bin:/usr/local/Garage:/usr/local/Garage/bin:/usr/local/:/Library/Apple/usr/bin
```

## Install code
Finally, after all of the above steps are completed, you can actually install the code for VirtualShip. You can technically use the GUI for this (it might be easier for some), but we've condensed all the steps into shell code. First we will need to navigate to the correct directory:
```
cd /usr/local
```
Next, we will need to download all the code from all branches in this repository, then move it into the Warehouse folder, then extract the correct files. In order to do this, we must run a series of commands (it might ask for your password):
```
cd /usr/local/Warehouse
sudo curl -LJO https://github.com/VirtualShip/Core/archive/v1.1.0-beta.zip
unzip Core-1.1.0-beta
sudo mv /usr/local/Warehouse/Core-1.1.0-beta/* /usr/local/Warehouse
sudo rm -rf -d Core-1.1.0-beta
sudo rm -rf Core-1.1.0-beta.zip
```
Now that you've extracted all the code, we will need to make the ```ship```, ```gh```, and ```gdrived``` files executable. To do this, run the following:
```
sudo chmod +x bin/ship
sudo chmod +x bin/gdrived
sudo chmod +x bin/gh
```
And you've successfully installed VirtualShip!
