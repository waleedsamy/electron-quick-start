# Electron Hello World

A quick way to get a Hello World Electron app running locally. and interact with host machine, like running application or load files.

## How To

### 1. clone this repo

```
git clone git@github.com:ngoldman/electron-hello-world.git
```

### 2. `cd` into the repo directory and run `npm install`

```bash
cd electron-hello-world
# download teamviewer get.teamviewer.com/traffics
# put it inside current directory
npm install
```

### 3. run `npm start`

```
npm start
```

### build for windows

```
npm run build-win
```

### if you don't have windows machine

```
vagrant up
```
If everything went well you should be staring in awe at a Hello World application. Yay!


### HOW It Work

### 1. TeamViewerQS(.exe, .app) should be existed in your project path
### 2. import required modules
```
 var child_process = require('child_process');
 var appPath = process.resourcesPath + "/app/";
```
### 3. `executeTVWin` will get `TeamViewerQS.exe` and start it as
 ```
 function executeTVWin() {
     var executablePath = appPath + 'TeamViewerQS.exe';
     child_process.execFile(executablePath);
 }
 ```
### 4. `executeTVMac` will get `TeamViewerQS.app` and start it as
 ```
 function executeTVMac() {
     var executablePath = appPath + 'TeamViewerQS.app';
     child_process.exec('open -a ' + executablePath);
 }
 ```
### 5. call `executeTVWin` or `executeTVMac` to start TeamViewer app on windows or Mac respectively.

## Learn more

This demo is based on instructions and code from the Electron [Quick Start tutorial](https://github.com/atom/electron/blob/master/docs/tutorial/quick-start.md).

To find out more check out the Electron [website](http://electron.atom.io/) and [documentation](https://github.com/atom/electron/tree/master/docs).

## License

[CC-0](LICENSE.md)
