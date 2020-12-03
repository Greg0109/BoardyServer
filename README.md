# Boardy
Sync the clipboard with your PC!

Long gone are the days where using a discord bot was the only way to send data from the phone to the pc easily or using email, introducing Boardy:
Boardy is a tool that allows you to seamlessly sync your clipboard with your PC. It can:
- Sync text between PC and the iPhone (both ways)
- Copy an image from the iPhone to the PC (the other way around is not supported yet). 

It features a custom made server that must be installed on the PC for the tweak to work properly.
You need to download the server that is made for your OS (see the folders on this github), and also you need to download the ServerConfig.json file, which **NEEDS** to be placed on the same folder as the server executable.

The iOS tweak can be found in [Chariz](https://chariz.com/buy/boardy)

## Before you launch the server
Please make sure you have the ServerConfig.json file **on the same folder as the executable**. If you don't know how to download the .json file, you can download the entire github repo on a zip file using this [link](https://github.com/Greg0109/BoardyServer/archive/master.zip)

Edit the ServerConfig file with your iOS device's info (user and password for SSH, the default ones are root and alpine (you should change the password if its alpine))

If you are interested in copying images from the device to your PC, on linux and macOS you will need to install a tool called xclip (from macOS that tool can be installed using brew)
On windows there's no need for extra tools like that.

### IF YOU ARE USING macOS
If you are using macOS, you need to give permissions to the server before launching. 
You have to do so using the following command on terminal:
```chmod -R 755 Path/To/The/BoardyServer.app```
Change Path/To/The/BoardyServer.app to the path where the boardy server is located on your mac

### Copying Images
Keep in mind that copying images only works from the iOS device -> PC at the moment. This might change in a future update.
Also, the images cannot just be pasted to a folder, they must be pasted somewhere where an image can go, this means a image editor, a messaging app or a office document.

In order to share images on macOS, you must install the tool xclip (using [brew](https://brew.sh/)) along the tool [XQuartz](https://www.xquartz.org/)

### Warning:
 Keep in mind that some public wifis (just like coffee shops, universities and so on) usually have their ports blocked. This tweak might not work on such wifis.
 The server runs with **no UI and in the background**. This means that when you launch the server you will get no visual feedback. Try to copy something and see what happens. If you still prefer some visual feedback, you can open the activity manager of your computer to see if the server is running. Look for BoardyServer.

## If you want the server to autostart when you boot your PC.
### Windows
1. Press windows key + r
2. Copy the run command Shell:common startup
3. It will reach C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup
4. Creat the shortcut of the program you want to run in startup.
5. Drag and drop.
6. Restart the computer. 

## Linux
You can either use a cronjob to start the executable or use the StartUp applications that come with the distro (this may change depending on the distro you use).

## macOS

Following the instructions of: https://www.idownloadblog.com/2015/03/24/apps-launch-system-startup-mac/

1. Open System Preferences.
2. Click Users & Groups.
3. Click Login Items. At the bottom left corner of the window, click on the lock icon and enter your admin password.
4. Click the ‘+‘ sign and find the Application that you wish to auto-start via the Finder interface. You probably want to open the /Applications folder to do so. You can select multiple items by holding down the ⌘ key while selecting each item.
5. Once your desired items are selected, click the Add button.

## Where can I find my ip/hostname?
It's better if you put a .local at the end of the hostname in the server and tweak settings

### iOS
Follow the instructions in this [link](https://www.businessinsider.com/how-to-find-ip-address-on-ipad)

### Windows
How to find:
  
[-ip](https://support.microsoft.com/en-us/windows/find-your-ip-address-f21a9bbc-c582-55cd-35e0-73431160a1b9)
  
[-Hostname](https://kb.iu.edu/d/avza#:~:text=From%20the%20Start%20menu%2C%20select,the%20machine%20without%20the%20domain.)

### macOS
How to find:
  
[-ip](https://www.hellotech.com/guide/for/how-to-find-ip-address-on-mac)
  
[-Hostname](https://support.apple.com/guide/mac-help/find-your-computers-name-and-network-address-mchlp1177/mac#:~:text=Find%20your%20computer's%20local%20hostname&text=Bonjour%2Dcompatible%20services.-,On%20your%20Mac%2C%20choose%20Apple%20menu,System%20Preferences%2C%20then%20click%20Sharing.&text=Your%20computer's%20local%20hostname%20is,the%20top%20of%20Sharing%20preferences.)

### Linux:
If you're using linux, you should know how to set it up anyway