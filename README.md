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
Please make sure you have the ServerConfig.json file **on the same folder as the executable**

Edit the ServerConfig file with your iOS device's info (user and password for SSH, the default ones are root and alpine (you should change the password if its alpine))

If you are interested in copying images from the device to your PC, on linux and macOS you will need to install a tool called xclip (from macOS that tool can be installed using brew)
On windows there's no need for extra tools like that.

### IF YOU ARE USING macOS
If you are using macOS, you need to give permissions to the server before launching. 
You have to do so using the following command on terminal:
```chmod -R 755 Path/To/The/BoardyServer.app```
Change Path/To/The/BoardyServer.app to the path where the boardy server is located on your mac

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