# TenableCTF-Play-Me-Writeup
Writeup for Play me challenge at Tenable CTF 2021

This challenge is solvable in many different ways. Here are two methods I used.


## The Easy Way
You can access the game by loading the gb file into any gameboy emulator. 
[BGB](https://bgb.bircd.org/) works well for this because it lets you directly view and modify the ram as the game is running.
For this method, that functionality isn't necessary, so pick whichever one you want.

.![](https://github.com/jwwood3/TenableCTF-Play-Me-Writeup/blob/main/StartScreen.jpg)

The game's controls are fairly simple, directional input for movement, B to jump, and hold A to run. Note that these controls are
usually mapped to the keyboard differently for each emulator. BGB by default uses arrow keys for movement, enter for start, S for A, and A for B.
To start, simply jump and dash your way over the platforms. Beware, this isn't mario, platforming can be tricky. Luckily, this is a "tool-assisted" run,
so you can make use of the save and load state functions in your emulator of choice. With enough time, dedication, and just the right amount of cheating,
even the most casual of gamers should be able to reach this point here.

.![](https://github.com/jwwood3/TenableCTF-Play-Me-Writeup/blob/main/HaHaScreen.jpg)

This is where it gets tricky. You've likely honed your platforming skills enough to this point that you'll easily gauge the distance and
jump to land on the next block. Only to fall through this sinister fake platform placed here specifically to confound gamers of your skill level as the
disembodied background text laughs at your failure.

Don't give up, though. There is a solution. If you hold the dash button while you attempt this final jump, your character will perform
what is colloquially known as a "pro gamer move," and easily clear the fake platform entirely, hitting the edge of the screen behind it.
Once you've gotten this far and proved your skill with a leap of faith into the unknown, the game will reward you with the flag.

.![](https://github.com/jwwood3/TenableCTF-Play-Me-Writeup/blob/main/flagScreen.jpg)

## The Hard Way
This route is a little more technical. BGB also includes the ability to look at the visual assets of the game under VRAM viewer.

.![](https://github.com/jwwood3/TenableCTF-Play-Me-Writeup/blob/main/VRAM_viewer.jpg)

Here, you can see the textures used to make up all the background text in the game in the block of 128 tiles at the bottom.
You can extract these tiles in a screenshot, split them up into separate files, and paste them somewhere you can more easily move them around.
Here, I'm using Google slides.

.![](https://github.com/jwwood3/TenableCTF-Play-Me-Writeup/blob/main/scrambled.jpg)

This may look like a mess, but you can rearrange these (preserving their original orientation) to form the flag as it is displayed in the game (roughly).

.![](https://github.com/jwwood3/TenableCTF-Play-Me-Writeup/blob/main/assembled.jpg)
