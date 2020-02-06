# bing-wallpaper-for-mac
Bing wallpaper for mac

This program is written in python specifically for MacOS and tested on Catalina 10.15.1 running python 2.7.16 and is based upon bing-wallpaper-for-mac by an original work by Bobin Joseph (see LICENSE.md).

###Installation
-  To install, copy the app into your /Applications folder or into your ~/Applications folder according to preference.
-  To refresh the wallpaper automatically, you can run one of the scripts provided in the Scripts folder that will install a plist file into your LaunchAgents folder.

###Uninstall
- First run the provided uninstall script to stop auto refreshing the wallpaper
- Then delete the app from your Applications folder
- Optionally delete the `~/Pictures/bing-wallpaper` folder and its contents


###Notes
-  The app is written in python and is embedded in an Automator application.
	- The checker script checks to ensure there is internet connectivity, then checks to see if an image file already exists in the ~/Pictures/bing-wallpaper folder.
		- If there are files, it will check to see if the file was created today.
			- If the file was created today, it stops and doesn't do anything
			- Otherwise, it runs the script to download the wallpaper.
		- If there are no files, it runs the script to download the wallpaper
-  The original script saved space by only keeping 1 image in the ~/Pictures/bing-wallpaper folder. I preferred to keep previous images and remove them manually so I modified the default behavior accordingly.