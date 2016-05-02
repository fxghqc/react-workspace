# react-workspace
 vagrant powered react dev environment

### Requirements
1. vagrant
1. VirtualBox and VirtualBox Extension Pack

### Config
```bash
vagrant plugin install vagrant-guest #（需要翻墙）

git clone https://github.com/fxghqc/react-workspace.git
cd react-workspace

# change forwarded_port and synced_folder
vim Vagrantfile

vagrant up # waiting a few minutes
vagrant ssh

cd *synced_folder*
npm i --no-bin-links #（需要翻墙）
```
