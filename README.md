*******************************************************************************
*********************** Gohan Ethermine Scripts Package ***********************
*******************************************************************************

Debian based distros only, as these scripts rely heavily on apt.
Tested to be functional on Ubuntu Server 16.04 LTS and Mint 18.2.q

INSTALLATION:

- Download this package to your $HOME directory on Linux 
(git clone https://github.com/xcalibur839/ethscripts.git ~/mining)
- Change to the setup directory (cd ~/mining/setup/)
- Set the permissions of the setup script (chmod +x setup)
- Run the setup script (./setup)

You will be asked for your password to continue. Once setup has completed,
you can install the proper drivers for your graphics card(s) by running the
approprate install script(s) from the setup directory:
("./install AMD drivers") AND/OR ("./install NVIDIA drivers")

Once the setup has completed and the drivers are installed, reboot the
computer. There will be 3 new scripts in your $HOME folder. 

(optional) To setup the Sensors program, run the detect temp sensors script in
the setup directory, and reboot the computer:
(sudo "~/mining/setup/detect temp sensors") then (sudo reboot)

Download the mining software that you wish to use by following these steps:
- Navigate to the ethereum mining github releases page:
https://github.com/ethereum-mining/ethminer/releases
- Copy the link for the Linux .tar.gz file for the version you wish to use.
- Use the copied URL as the parameter for the getNewMiner script
(~/getNewMiner https://git.io/vpYQA)
- Repeat these steps each time you would like to use a different miner version.
- You can also run getNewMiner without any parameters to revert to the previous
version of the mining software (~/getNewMiner)

You will also need to configure the config.txt file to point to your wallet and
to include any other options.

- Open the config.txt file in your favorite Linux text editor
(nano ~/mining/config.txt) OR (vim ~/mining/config.txt)

Reboot your machine to ensure everything loads properly (sudo reboot)

USAGE:

- Run the start script in the $HOME directory to begin mining in a GNU screen
session (~/start)
- To update the machine, run the update script in the $HOME directory and enter
your password (~/update)

Press Ctrl + a and then " (quotation mark) to view the default list of windows:
- Mining: Displays the ethminer output
- HTOP: A more user friendly top. Similar to task manager on Windows.
- Watch Sensors: Displays temperature sensors. (Requires manual setup)
- bash: A standard bash prompt

For more information on how to use GNU screen, search online for commmands or
see the built in manual (man screen).