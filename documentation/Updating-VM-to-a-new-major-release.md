# Updating the VM
In most cases, typing `update_VM.sh` in a terminal will be sufficient to update the software. However, for some upgrades, extra system or Python packages can be required which were not preinstalled on the VM of a previous version. You can install these as follows
```sh
cd ~/devel/SyneRBI_VM
git pull
cd scripts
sudo -H ./INSTALL_prerequisites_with_apt-get.sh
sudo -H ./INSTALL_python_packages.sh
sudo -H ./INSTALL_CMake.sh
./configure_gnome.sh
update_VM.sh
```
## VM for specific training events
In some cases, we create a VM for a specific training school. The configuration for such an event will be on a specific branch. For instance for the Synergistic Reconstruction training school November 2019, please do the following before the `git pull` mentioned above
```sh
git fetch
git checkout Symposium2019