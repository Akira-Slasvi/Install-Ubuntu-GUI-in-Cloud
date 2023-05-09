# Install-Ubuntu-GUI-in-Cloud
Install Ubuntu GUI in Cloud
# Update and upgrade library
sudo apt update && sudo apt upgrade -y
# Install Ubuntu Desktop resources
sudo apt-get install ubuntu-desktop xrdp stacer -y
# Remove unnecessery firewall rules
sudo cp /etc/iptables/rules.v4 /etc/iptables/rules.v4.bak && sudo truncate -s 0 /etc/iptables/rules.v4
# Remove free desktop policy
sudo rm /usr/share/polkit-1/actions/org.freedesktop.color.policy
# Create your own password
sudo passwd ubuntu 
//Yourpassword

# Turning Animations off in Ubuntu 
================================
gsettings set org.gnome.desktop.interface enable-animations false

If for any reason you would like to turn these Animations, effects and transitions back on again the command is :
gsettings set org.gnome.desktop.interface enable-animations true

# Reduce the number of colors that XRDP has to transmit.
======================================================
sudo sed -i 's/max_bpp=32/max_bpp=16/g' /etc/xrdp/xrdp.ini && sudo reboot

Again, If for any reason you would return to the full colours being transmitted by XRDP :
sudo sed -i 's/max_bpp=16/max_bpp=32/g' /etc/xrdp/xrdp.ini && sudo reboot

