# foldingathome.org
Folding@home Installation on Google Cloud Platform on a Ubuntu 22.04 LTS machine

## Installation
- Step 1: Visit https://cloud.google.com/ and register for a Google Cloud account.
- Step 2: After registering, you will be taken to the Compute Engine section. Create a new virtual machine by clicking on "Create instance".
- Step 3: Name your virtual machine and set its location.
- Step 4: When setting up your virtual machine, choose the "General purpose" option and select "N1 (standard, Intel Skylake)" as the machine type. Then, under the "machine type" section, select "f1-micro" for the cheapest option.
- Step 5: For the boot disk, select "Public images" and choose the operating system of your choice. Keep in mind that all operating systems run from the terminal and do not have a graphical user interface. I currently use Ubuntu 22.04 LTS.
- Step 6: Enable HTTP and HTTPS for the virtual machine.
- Step 7: After creating the virtual machine, click on the "SSH" icon to open a terminal window in your browser.
- Step 8: In the terminal, run the following commands
```
sudo apt update
sudo apt upgrade
```
- Step 9: Open a terminal window and type the following command to create a new directory called "foldingathome.org" and navigate into it:
```
mkdir foldingathome.org && cd foldingathome.org/
```
- Step 10: Download Folding@home client by typing command below (I use v7.4):
```
wget --no-check-certificate https://download.foldingathome.org/releases/public/release/fahclient/debian-testing-64bit/v7.4/fahclient_7.4.4_amd64.deb
```
- Step 11: Install the Folding@home client by typing the following command:
```
sudo dpkg -i --force-depends fahclient_7.4.4_amd64.deb
```
- Step 12: When prompted, enter your Folding@home username, passkey, and team number:
```
Username: <your_username>
Passkey: <your_passkey>
Team: <your_team_number>
```
- Step 13: Finally, check the status of the Folding@home client by typing the following command:
```
sudo /etc/init.d/FAHClient status
```
This should show you the status of the Folding@home client, including whether it is running, what work unit it is processing, and more. If everything is set up correctly, you should be able to start contributing to Folding@home immediately.
