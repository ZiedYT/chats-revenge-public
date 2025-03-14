# Chat's Revenge
## Twitch bits and channel points rewrds bot, by ZiedYT
[DM me for any issues](https://twitter.com/ZiedYT) :)
## Features
- Support for both channel points and bits
- Rewards:
    - Chat can timeout/untimeout each other
    - Chat can turn off your monitor
    - Chat can blur your monitor
    - Chat can rotate your monitor
    - Chat can minimize your current window
    - Chat can open popup windows
    - Chat can apply glitch effect to your game
    - Chat can make your game lag
    - Chat can shrink your game
    - Chat can pixelate your game
    - Chat can mute your mic
    - Chat can turn off your camera
    - Chat can simulate keyboard presses
    - Chat can disable your keyboard/mouse
    - Chat can invert your keyboard
    - Chat can playsounds
    - Chat can throw tomatos at your screen.
    - More to come :D
## Game Mods:
Game mods where chat can influence the game using bits.

- [Lethal Company](https://thunderstore.io/c/lethal-company/p/ZiedYT/ChatsRevenge/)
- [R.E.P.O](https://thunderstore.io/c/repo/p/ZiedYT/Chats_Revenge_REPO/)
- [Pokemon Firered](https://github.com/ZiedYT/chatsRevenge-firered/)

## Set up
- [If you want to use bits: add the extension to your channel](https://dashboard.twitch.tv/extensions/6fwhzhvt0ljihf9o1vzvjfp12jvkax)
- Configure the bits rewards you want to add
- [Download the zip of the lastest release](https://github.com/ZiedYT/chats-revenge-public/releases/latest). password: `verystrongpassword`
- Extract the zip.
- Run chatsRevenge.bat (or as admin run chatsRevenge_main/chatsRevenge_console.exe if the other one doesnt run)
- A window will open, go to the second tab (credentials)
    - Type your channel name
    - Press the get token button (dont show stream)
    - Authorize and copy the token
    - Paste the token in the second field
- To use and configure channel points:
    - Open the third tab
    - Here you can press the create reward button to add a reward in your channel
    - You can specify the title, description and cost
    - Create the rewards you want to use
- Open the first tab:
    - If you want to use a reward, make sure the checkbox is ticked. (this only affects the channel points rewards)
    - You can specify some parameters like the duration etc...
- If you want to use the "rotate monitor" ,"mute mic", "turn off cam","Throw tomatos" rewards, Open OBS:
    - Add Lua script by: Tools > Scripts > "+"
    - Select "lua/chatsRevenge.lua"
    - Type the name of your monitor source that you want chat to rotate (So that It will rotate for you and chat).
        - Right click on the source > Transform > Edit Transform > Positional allignment: center.
    - Type the name of your camera source that you want chat to turn off
    - Type the audio source (mic) you want chat to mute
    - Type the tomato throwing overlay name
- If you want to use the tomato throwing reward:
    - Add this as a browser source to your obs `https://github.com/ZiedYT/chatsRevenge-TomatoThrow`
    - If you didn't already, add the Lua script and type your tomato overlay name
    - Credits to [abdullahmorrison](https://github.com/abdullahmorrison/erobb221-twitch-extension/tree/main). I used his repo as a template for the tomatos
- If you want an overlay that shows your chat what effect is currently running, you can add this to your OBS as a source: http://localhost:23337/
  
## Advice
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
- Window Effects:
    - Chat can apply effects (shrink, pixelate, lag, glitch) the game window.
    - You have to select your monitor that chat sees and select the game window
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
    - To add sounds:
        - Creating a pastebin link
        - Uploading an mp3 to audio.jukehost.co.uk, copy its link
        - Add a new line in your pastebin, eg, file_name = drive_url
        - Copy the pastebin link in the field provided in the program/ extension dashboard(and select the bits amount)
    - Chat has to type the file name to play the sound (or a random one will be selected)
- Popups:
    - To add the images used by the popups:
        - create a pastebin
        - upload images to a image hoting website
        - copy and paste the link in the pastebin
        - make sure each link of every image is in a new line
        - copy the pastebin link to the field

