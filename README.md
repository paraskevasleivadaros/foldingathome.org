# 🦠 foldingathome.org
Folding@home Installation on Google Cloud Platform on a Ubuntu 22.04 LTS machine

### Installation
Visit https://cloud.google.com/ and register for a Google Cloud account.

After registering, you will be taken to the Compute Engine section. Create a new virtual machine by clicking on "Create instance".

Name your virtual machine and set its location.

When setting up your virtual machine, choose the "General purpose" option and select "N1 (standard, Intel Skylake)" as the machine type. Then, under the "machine type" section, select "f1-micro" for the cheapest option.

For the boot disk, select "Public images" and choose the operating system of your choice. Keep in mind that all operating systems run from the terminal and do not have a graphical user interface. I currently use Ubuntu 22.04 LTS.

Enable HTTP and HTTPS for the virtual machine.

After creating the virtual machine, click on the "SSH" icon to open a terminal window in your browser.

In the terminal, run the following commands
```shell
sudo apt update
sudo apt upgrade
```
Open a terminal window and type the following command to create a new directory called "foldingathome.org" and navigate into it:
```shell
mkdir foldingathome.org && cd foldingathome.org/
```
Download Folding@home client by typing command below (I use v7.4):
```shell
wget --no-check-certificate https://download.foldingathome.org/releases/public/release/fahclient/debian-testing-64bit/v7.4/fahclient_7.4.4_amd64.deb
```
Install the Folding@home client by typing the following command:
```shell
sudo dpkg -i --force-depends fahclient_7.4.4_amd64.deb
```
When prompted, enter your Folding@home username, passkey, and team number:
```shell
Username: <your_username>
Passkey: <your_passkey>
Team: <your_team_number>
```
Finally, check the status of the Folding@home client by typing the following command:
```shell
sudo /etc/init.d/FAHClient status
```
This should show you the status of the Folding@home client, including whether it is running, what work unit it is processing, and more. If everything is set up correctly, you should be able to start contributing to Folding@home immediately.

### 🛠️ Tech Stack
[![Linux](https://skills.thijs.gg/icons?i=linux)](https://linux.org/)
[![GCP](https://skills.thijs.gg/icons?i=gcp)](https://cloud.google.com/)

### ©️ Copyright & License
[MIT](https://github.com/paraskevasleivadaros/foldingathome.org/blob/master/LICENSE)
