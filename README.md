# Establish-RDP-connection-to-linux-VM-


https://docs.microsoft.com/en-us/azure/virtual-machines/linux/use-remote-desktop


1. establish ssh connection via putty
2. sudo apt-get update
   sudo apt-get -y install xfce4
3. sudo apt-get -y install xrdp
   sudo systemctl enable xrdp
4. echo xfce4-session >~/.xsession
5. sudo service xrdp restart

6. (optional if didnt create a password for this vm) : sudo passwd azureuser

7. (do this from azure cli (cloud shell)) : az vm open-port --resource-group myResourceGroup --name myVM --port 3389
Note : I did manual adding of port 3389 from inbound security rules

8. From remmina set the default color depth to high color(16 bpp) and then proceed.
https://gitlab.com/Remmina/Remmina/issues/1584

Final step . Go to connect in azure portal and download andd open the RDP file under the RDP section.
Log in and enjoyyy
