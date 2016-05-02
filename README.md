# react-workspace
 vagrant powered react dev environment in windows.

### Requirements
1. vagrant
1. VirtualBox and VirtualBox Extension Pack

### Config
```bash
vagrant plugin install vagrant-guest # （需要翻墙）

git clone https://github.com/fxghqc/react-workspace.git
cd react-workspace

# change forwarded_port and synced_folder
vim Vagrantfile

vagrant up # waiting a few minutes
vagrant ssh

cd *synced_folder*
npm i --no-bin-links # symlinks won't work in the shared folder（需要翻墙）
```

### Note
Webpack dev server hot reload and hmr not works in a shared folder. The watchers for Linux don't work on windows files, use watch poll to checks every x ms if a file changed. Add this options into dev server/middleware configuration.
```javascript
watchOptions: {
  aggregateTimeout: 300,
  poll: 1000
}
```


### Thanks
[ocombe](https://github.com/webpack/webpack-dev-server/issues/155#issuecomment-166902532)
