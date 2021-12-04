# Mac-Lessons-Learned
List of lessons learned as switching from Windows to Mac

- Move instead of copy in the finder: Hold CMD while drag and drop
- Set a monitor as primary: System Preferences > Display > Drap little white bar to desired primary monitor
- Prefer ethernet over wi-fi: System Preferences > Network > Click the little ... menu button > Set service order > Drag ethernet to top > OK > Click Apply button!
- Move a word at a time or mark a word at a time: ALT + ARROW / ALT+SHIFT + ARROW
- Prevent any application from adjusting the microphone level:
  1. Open the 'Audio MIDI Setup' application
  2. In the bottom left corner, click the + symbol and select Create aggregate device
  3. Select the new aggregate device, then tick the check in the Use column for your real microphone.
  4. Rename the new aggreate device to something useful so you know which one it is.

- Unable to "browse" the file system like in Windows File Explorer: Finder > Preferences > Sidebar > Put checkbox next to local computers name. Potentially add to finder favorites.
- Finder folders not sorting at the top: Finder > Preferences > Advanced > Keep folders on top > In windows when sorting by name
- CMD-TAB only shows apps, not windows of individual apps. Making it difficult to switch from one Google Chrome window to another. Use free ALT+TAB app: https://alt-tab-macos.netlify.app/
- Scroll whell is reversed: https://pilotmoon.com/scrollreverser/
- Easy SSH to remote hosts using keypair:
  1. Create folder ~/.ssh
  2. Move .pem file from fx AWS here
  3. Run command: ssh-add -K ~/.ssh/your-private-key.pem
  4. Create ~/.ssh/config file if it does not exist and add:
 > Host *  
 >  UseKeychain yes  
 >  AddKeysToAgent yes  
 >  IdentityFile ~/.ssh/your-private-key.pem  

- SSH certificate (.pem) files should be chmod 600 to avoid THIS IS UNSAFE errors preventing them from being used.
- Default mail client should be Outlook, not Apple Mail: Open "Mail" app -> Preferences -> General -> Select Microsoft Outlook.
- Add SharePoint location to local Finder window: http://www.mndi.ca/index.php/support/microsoft-sharepoint/14-add-a-sharepoint-folder-in-osx-10-6-x
- Stop creating .DS_Store files, execute terminal command: defaults write com.apple.desktopservices DSDontWriteNetworkStores true
- Missing add-ons in Microsoft Outlook such as corporate "Report Phish" button. Enable "Optional Connected Preferences" in the Outlook App menu > Preferences > Privacy
- Show ping statistics without stopping ping: CTRL+T
- List network interfaces: networksetup -listallhardwareports
- GeforceNOW cloud gaming platform suffers periodical lag if the Mac has location services enabled. Must be completely disabled.
- Stop Chrome from changing mail handler to for example outlook.com webapp: chrome://settings/handlers and set to "Don't allow sites to handle protocols".
- When recording, the menu bar can be annoying at the top of the shared screen. Make it automatically hide in System Preferenes > Dock & Menu > "Automatically hide and show the menu bar"
- Custom DNS resolution for a single domain can be handled by creating a new folder /etc/resolver and a file per domain inside such as /etc/resolver/rasmushaslund.com
- Install PowerCLI: Install-Module -Name "VMware.PowerCLI" -Scope "CurrentUser"
- Cut and Paste files in Finder: COMMAND+C to "Copy" or "Cut", then COMMAND+OPTION+V to "Paste with cut from source"

Unsolved problems:
- RIGHT_OPTION+2 = @
- OBS full screen preview starts in a new "OBS" space rather than the "Default" space on that screen.
