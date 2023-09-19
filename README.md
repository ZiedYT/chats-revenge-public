# Chat's Revenge
## Twitch bits and channel points rewrds bot, by ZiedYT
DM me for any issues :)
## Features
- Support for both channel points and bits
- Rewards:
    - Chat can timeout/untimeout each other
    - Chat can turn off your monitor
    - Chat can blur your monitor
    - Chat can mute your mic
    - Chat can rotate your monitor
    - Chat can minimize your current window
    - Chat can turn off your camera
    - Chat can simulate keyboard presses
    - Chat can disable your keyboard/mouse
    - Chat can playsounds
    - More to come :D
## How To Use
- Download the zip of the lastest release [here](https://github.com/ZiedYT/chats-revenge-public/releases)
- Extract the zip
- As admin, run chatsRevenge.exe (or chatsRevenge_console.exe if the other one doesnt run)
- A window will open, go to the second tab (credentials)
    - Type your channel name
    - Press the get token button
    - Authorize and copy the token
    - Paste the token in the second line
- Open the third tab:
    - Here you can press the create reward button to add a reward in your channel
    - You can specify the title, description and cost
    - Create the rewards you want to use
- Open the first tab:
    - If you want to use a reward, make sure the checkbox is ticked. (this only affects the channel points rewards)
    - You can specify some parameters like the duration etc...
- Add the bits extension to your channel [here](https://dashboard.twitch.tv/extensions/6fwhzhvt0ljihf9o1vzvjfp12jvkax-0.0.1), and configure the bits rewards you want to add
- Open OBS:
    - Add Lua script by: Tools > Scripts > "+"
    - Select "chatsRevenge.lua"
    - Type the name of your monitor source that you want chat to rotate (So that It will rotate for you and chat).
        - Right click on the source > Transform > Edit Transform > Positional allignment: center.
        - DO THIS FOR EVERY SCENE WITH THIS MONITOR
    - Type the name of your camera source that you want chat to turn off
    - Type the audio source (mic) you want chat to mute
- If you want an overlay that shows your chat what effect is currently running, you can add this to your OBS as a source: http://localhost:23336/
- Advice:
    - First Tab:    
        - The stackable checkbox affects both channel points and bits
        - The other configurations on the first tab affect only affects channel points
    - Configure the bits parameters (eg: duration) in the extension dashboard:
        - You can create multiple variations each with their bits amount:
          - Example: Multiple timeout options, the longer the duration the more bits are needed
      - IF YOU ARE USING TWO VARIATIONS OF THE SAME ACTION (EXAMPLE BITS AND CHANNEL POINTS) MAKE SURE THE STACKABLE PARAMETER IS ON
- More Info:
    - If you minimize the window you will find the program in your tray, right click it    
    - fail-safe: press on esc+q and the current effects will expire
    - Camera:   
        - Allow chat to temporarily disabled your camera.     
        - For this, you have to set up the lua script in OBS as mentioned above.
        - You can specify the duration for which the camera will be disabled
        - You can specify if the duration is stackable
    - Mute:
        - Allow chat to temporarily mute your OBS audio source.
        - You need to set up the lua script in OBS as mentioned above.
    - Monitor:
        - Allow chat to temporarily disable/blur/rotate your monitors.
            -  For monitor rotation, make sure to set up the lua script in OBS as mentioned above. (so that it rotates for chat as well)
        - You can specify the duration for which the monitors will be affected
        - You can specify if the reward is stackable
    - Timeouts:
        - Allow chat to timeout each other.
        - Doesn't work on mods/vips
        - If you want to prevent more specific users from getting banned, make a text file named "immune.txt", and type the name of the users, each name in a new line
        - You can specify the duration for which the the chatter will be timed out for.
        - You can specify if the duration is stackable, ie the new time out duration = time left in the previous timeout + duration specified
    - Untimeouts:
        - Allow chat to remove timeouts
    - Keyboard:
        - Allow chat to simulate keyboard presses.
        - You can specify the duration of the key press
        - You can specify if the duration is stackable
        - You can choose which of the special keys can be simulated: alt, shift, ctrl, esc, enter, tab, function keys(f1, f2...)
    - Playsounds:
        - To add a sound:
            - Creating a pastebin link
            - Uploading an mp3 to audio.jukehost.co.uk, copy its link
            - Add a new line in your pastebin, eg, file_name = drive_url
            - Copy the pastebin link in the field provided in the program/ extension dashboard(and select the bits amount)
        - Chat has to type the file name to play the sound (or a random one will be selected)

