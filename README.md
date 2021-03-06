# Better OoT


This is a ROM patcher for _The Legend of Zelda: Ocarina of Time_ that applies various quality-of-life changes to the game. These changes are implemented with various speedrun categories in mind.


This is an extension of an idea initially created by Moltov. This project aims to further allow the user to customize their settings and preserve most aspects of all main speedrunning categories.


This project is based off of the 3.0 version of the Ocarina of Time Randomizer. Many new features were added, and many details were tweaked to preserve details of speedrun routes.


## Download and Install

Download the appropriate version for your system from the [releases page](https://github.com/fig02/Better-OoT/releases).

Windows 10: Download "BOoT-Windows10.zip" and extract the contents of the zip folder to your location of choice. Double click BetterOoT.exe (the app with the ocarina icon) to run.

Windows 8/7/Vista/XP: Download "BOoT-WindowsOther.zip" and extract the contents of the zip folder to your location of choice. Double click BetterOoT.exe (the app with the ocarina icon) to run.
(If youre on windows 10 you can run this version too. It just has more files, so it is a bit more cluttered than the win10 release)

Mac/Linux: Bundled versions are not supported for these operating systems. You will need to download and install [python 3.7](https://www.python.org/downloads/) and run from source. Download BOoT-Source.zip and run the Gui.py python script.


## Usage

After opening Better OoT you will be greeted by a ROM patcher. This patcher has 3 tabs which you can use to tweak the settings to your liking.

### ROM Tab
This tab is where you specify file information for the patcher.

**Base ROM**: Path to an English Vanilla 1.0 OoT ROM. This is the ROM the patcher will use a base. You must supply your own ROM, one is not included with this program.

**Base WAD**: Path to a English Vanilla 1.2 OoT WAD. This is only necessary if you are patching a WAD for use on VC. If you are making a WAD remember to still supply a ROM too. You must supply your own WAD, one is not included with this program.

**Output Directory**: Path for the output of the program. By default, this is set to an "Output" folder in the Better OoT folder. If this folder does not exist, the patcher will create it.

**Output File Type**: You can choose from creating a ROM or a WAD. Select ROM if you are playing on N64/Emulator. Select WAD if you are playing on Wii Virtual Console. If you select WAD you must supply a base WAD in the field above.

### Options Tab
This tab is where you specify settings that will affect gameplay.

**Remove Area Intro Cutscenes**: Listed are checkboxes for most area introduction cutscenes in the game. These are customizable because they can influence speedrun routes depending on the category. For example: Glitchless would want to keep the Gerudo Fortress cutscene because of the guard cycles, while other categories would want to get rid of it. Uncheck a box to add the intro cutscene for that area back.

**Skip Intro Cutscene**: With this checked, the cutscene played at the beginning of a new file will be skipped. You will immediately spawn in links house.

**Skip Forest Elevator Cutscene**: Toggle if the cutscene in Forest Temple plays where the Poe Sisters bring the elevator down. It is desirable to add this back mainly for the 100% category

**Skip Nabooru Defeat Cutscene**: Toggle if the Nabooru Knuckle cs plays when defeating her. This is toggleable because you can skip it with glitches.

**Fast Blue Warp Cutscenes**: Speed up all cutscenes that play when entering a dungeon blue warp. Note that Wrong Warps still work when this option is enabled.

**Fast Song Cutscenes**: When learning songs you will immediately be prompted to play the song. This is toggleable because you can skip most of these cutscenes with glitches.

**Fast Chest Cutscenes**: Link will kick open all chests regardless of size.

**Remove Owls**: Owl triggers will be removed. Note that this effects time of day.

**Quick Boots**: With this enabled Hover Boots and Iron Boots will be toggleable on the dpad without needing to pause the game. This is more of a fun extra feature that was made for rando and was requested to be included here too.

**Damage**: Choose between normal damage and one hit KO mode.

**Dungeon Quest**: Choose between Vanilla and Master Quest Dungeons.

**Default Targeting Option**: Hold Targeting is mandatory (Kappa)


### Cosmetics Tab
This tab is where you can customize visual settings for the game. These options will not affect gameplay in any way.

**Background Music**: Set the background music to normal, random, or none.

**Tunic Colors**: Set the color of the 3 tunics in the game. There are many pre-determined colors to choose from. Random choice will randomly choose one of these colors. Completely random will generate a random color.

**Navi Colors**: Set the color of Navi's many states. There are many pre-determined colors to choose from. Random choice will randomly choose one of these colors. Completely random will generate a random color.

**Low HP SFX**: Set the sound that will be played when Link is in critical health.

**Navi SFX**: Set the sounds that Navi will make when alerting you.


## Usage Details

There are some details with the hack that need to be emphasized.

**Time of Day**: The starting time of day is calculated based on 3 settings: Skip Intro, Skip Hyrule Field, and Skip Hyrule Castle. With these options enabled, the starting time of day is set later to account for these missing cutscenes. While useful in some cases, it can cause issues in others. For speedrun categories that do ESS Owl Skip or Aqua escape, you need to keep in one or both cutscenes to be able to make it to market in time. 

**No Continue After Death**: On Vanilla VC if you die in specific areas and no continue the game will crash. This happens on 1.0 VC, but in different areas. This is relevant for No IM/WW because if you "no continue" when dying in Sacred Forest Meadow as adult, the game will crash. Players on VC will need to savewarp normally. A fix may be found for this in the future, but it is a vanilla issue which is hard to debug as it is VC exclusive.

**Cutscene Pointers**: For categories that Wrong Warp it is important to keep area intro cutscenes that set the CS pointer for Wrong Warps (for example: Deku Intro for Ganondoor). Also, warp song cutscenes are skipped and thus do not set the pointer. This shouldn't be an issue in most categories and should be remedied by a save warp.

**Fast Song Cutscenes**: With this option enabled, the staff for learning songs will appear right away. This can cause a harmless bug where you can walk with the ocarina making noises. This can also make tricks like Deathless Bolero behave strangely. In cases like this you may want to disable this option.

**Short Chest Cutscenes**: This option is only an issue for the initial position Boatskip setup. However, targetting before opening the chests lets you do the setup as normal.

**Twinrova Defeat Scene**: After defeating Twinrova, the cutscene is sped up which causes some differences with the camera. The position and angle is the same as normal, but any setups that use the camera for an angle will not work. May potentially be fixed in later versions.

**Kakariko Gate**: Since the flag that opens the gate in Kakariko is shared with the flag that skips the Master Sword cutscene, the gate is forced closed. This is very minor and just adds a short cutscene for 100%.


## Changelog

For a list of changes made from the 3.0 version of Rando, check out [BOoT Changelog](https://github.com/fig02/Better-OoT/blob/master/Notes/BOoT_Changelog.txt) in the notes folder.

Below is summary of the changes made from the Vanilla version of the game:

- All text is quick text
- Song cutscenes are skipped (toggled)
- Dungeon blue warp cutscenes are shortened (toggled)
- All chest cutscenes are shortened (toggled)
- Warp song cutscenes are shortened
- Many unnecessary cutscenes are shortened or skipped
- Dampe is first try
- Truth spinner is first try (torch closest to hover boots)
- Bombchu bowling reward order is static
- Empty bomb glitch is patched
- Collection delay at Big Goron is patched
- Graves are patched to behave like 1.2
- Block pushing is sped up
- Kakariko carpenter moved so he is not in the way of the cucco route
- Starting time of day is dynamic depending on intro cutscene settings


## Thanks

Many people were directly or indirectly involved with this project.

Thank you to:

**Krimtonz**: For helping me implement many of the features, guiding me whenever I was stuck, and for allowing me to vent to him whenever I had an issue with something not working. This project would not have happened without him.

**Moltov**: For creating the original Better OoT and inspiring this project. This idea was his and I expanded on it to allow more flexibility.

**Glank/N3rdswithgame**: For teaching me MIPS Assembly and answering any questions I had about it.

**TestRunner/AmazingAmpharos/mzx/Grant/many others**: For the work done on the OoT Randomizer. The 3.0 version of Rando was used as a base for Better OoT. Much of the work done on that project persists through this one.

**zfg/Scurty/Dannyb/RTA**: For testing the project through its many stages of development and providing feedback.

**The OoT Speedrunning Community**: For expressing interest in this project and giving me a reason to work on it :)

Thank you all! Enjoy.