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
sudo passwd ubuntu //Yourpassword
