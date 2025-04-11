# Chat's Revenge
## Twitch bits and channel points chat integration bot, by ZiedYT
[DM me for any issues](https://twitter.com/ZiedYT) :)
## Features
- Support for both channel points and bits
- Rewards:
    - `Display Rewards`: (require display capture and not window capture on OBS)
        - Chat can turn off your monitor
        - Chat can blur your monitor
        - Chat can rotate your current window
        - Chat can minimize your current window
        - Chat can open popup windows (you can choose your the popup pictures, follow guide below)
        - Chat can apply glitch effect to your current window
        - Chat can lag your current window
        - Chat can shrink your current window
        - Chat can pixelate your current window
        - Chat can mirror your current window
        - Chat can invert your current window's colors
    - `OBS input Rewards`: (requires the additional lua script below)
        - Chat can mute your mic 
        - Chat can turn off your camera
    - `Input Rewards`:
        - Chat can simulate keyboard presses
        - Chat can disable your keyboard/mouse
        - Chat can invert your keyboard
          
    - Chat can timeout/untimeout each other
    - Game specific effects for:
        - [R.E.P.O](https://thunderstore.io/c/repo/p/ZiedYT/Chats_Revenge_REPO/)
        - [Schedule I](https://thunderstore.io/c/schedule-i/p/ZiedYT/Chats_Revenge_Schedule_I/)
        - [Lethal Company](https://thunderstore.io/c/lethal-company/p/ZiedYT/ChatsRevenge/)
        - [Pokemon Firered](https://github.com/ZiedYT/chatsRevenge-firered/)
    - More to come :D
- `By adding the Lua script you can choose if the software should automatically be launched when opening OBS` 
## Game Mods:
Game mods where chat can influence the game using bits.

- [Lethal Company](https://thunderstore.io/c/lethal-company/p/ZiedYT/ChatsRevenge/)
- [R.E.P.O](https://thunderstore.io/c/repo/p/ZiedYT/Chats_Revenge_REPO/)
- [Pokemon Firered](https://github.com/ZiedYT/chatsRevenge-firered/)
- [Schedule I](https://thunderstore.io/c/schedule-i/p/ZiedYT/Chats_Revenge_Schedule_I/)

## Set up
- [If you want to use bits: add the extension to your channel](https://dashboard.twitch.tv/extensions/6fwhzhvt0ljihf9o1vzvjfp12jvkax)
- Configure the bits rewards you want to add
- [Download the zip of the lastest release](https://github.com/ZiedYT/chats-revenge-public/releases/latest). password: `verystrongpassword`
- Extract the zip.
- Run setup once.
- Run chatsRevenge (or as admin run chatsRevenge_main/chatsRevenge_console.exe if you want to see if errors occur)
- A window will open
    - Type your channel name
    - Press the get token button (dont show stream)
    - Authorize and copy the token
    - Paste the token in the second field
    - The window hides in your task tray when minimized. 
    - The windows app needs to be running for the mods and effects to work.
    - 
- If you want to use the "mute mic", "turn off cam", rewards, Open OBS:
    - Add Lua script by: Tools > Scripts > "+"
    - Select "lua/chatsRevenge.lua"
    - Type the name of your camera source that you want chat to turn off
    - Type the audio source (mic) you want chat to mute
    - `By adding the Lua script the software will be automatically be launched when opening OBS`
- If you want to choose what shows up in the `open popups` reward you can either:
    - (Locally) On the windows app, go to `Settings` > press `Media Folder`. you can copy paste your images there.
      
    - (Remote) You can allow your moderators to remotely update the used images by:
        - [Creating a new paste bin] (https://pastebin.com/)
        - Uploading images to a image hosting website
        - Copying the `direct` image url (example: i.imgur.com/imageid.jpeg works, imgur.com/a/imageid doesnt work)
        - Pasting the image urls, each one in a new line
        - Saving the paste bin
        - On the windows app go to setting
        - Paste the pastebin url in the input field in the formal `https://pastebin.com/raw/{paste_bin_id}?nocache=1`
          
- If you want an overlay that shows your chat what effect is currently running, you can add this to your OBS as a source: http://localhost:23337/
  
## Advice
- Configure the parameters (eg: duration) in the extension dashboard:
- fail-safe: press on esc+q and the current effects will expire
## General effects: work everywhere, not limited to games.
- Camera:   
    - Allow chat to temporarily disabled your camera.     
    - For this, you have to set up the lua script in OBS as mentioned above.
- Mute:
    - Allow chat to temporarily mute your OBS audio source.
    - You need to set up the lua script in OBS as mentioned above.
- Monitor:
    - Allow chat to temporarily disable/blur/rotate your monitors.
    - You can specify the duration for which the monitors will be affected
- Window Effects:
    - Chat can apply effects (shrink, pixelate, lag, glitch) the game window.
- Timeouts:
    - Allow chat to timeout each other.
    - Doesn't work on mods/vips
    - You can specify the duration for which the the chatter will be timed out for.
- Untimeouts:
    - Allow chat to remove timeouts
- Keyboard:
    - Allow chat to simulate keyboard presses.
    - You can specify the duration of the key press
    - You can choose which of the special keys can be simulated: alt, shift, ctrl, esc, enter, tab, function keys(f1, f2...)

- Popups:
    - To add the images used by the popups:
        - create a pastebin
        - upload images to a image hoting website
        - copy and paste the link in the pastebin
        - make sure each link of every image is in a new line
        - copy the pastebin link to the field

