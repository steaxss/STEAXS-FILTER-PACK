==============================
DBD CONFIG FILES - README
==============================

This archive contains recommended configuration files/settings for Dead by Daylight.

Please read carefully before editing anything.

------------------------------
1. INPUT.ini
------------------------------

You need to add the following lines to your Input.ini file:

[/Script/Engine.InputSettings]
bEnableMouseSmoothing=False
bDisableMouseAcceleration=True
RawMouseInputEnabled=1

These lines are also available in the file:

"DBD CONFIG\ADD THIS TO YOUR INPUT.ini.txt"

Open that file, copy its content, then paste it at the very end of your Input.ini file.

Default location:

C:\Users\YOUR_USERNAME\AppData\Local\DeadByDaylight\Saved\Config\WindowsClient\Input.ini

You can also quickly access the folder by pressing Windows + R and typing:

%LOCALAPPDATA%\DeadByDaylight\Saved\Config\WindowsClient

Then open Input.ini with Notepad or any text editor.

------------------------------
2. GameUserSettings.ini
------------------------------

In GameUserSettings.ini, you need to manually edit your resolution settings according to your own monitor resolution.

Open:

GameUserSettings.ini

Then look for the resolution-related lines and replace them with your desired resolution.

Example for 2560x1440:

ResolutionSizeX=2560
ResolutionSizeY=1440
LastUserConfirmedResolutionSizeX=2560
LastUserConfirmedResolutionSizeY=1440
DesiredScreenWidth=2560
DesiredScreenHeight=1440
LastUserConfirmedDesiredScreenWidth=2560
LastUserConfirmedDesiredScreenHeight=1440

Example for 1920x1080:

ResolutionSizeX=1920
ResolutionSizeY=1080
LastUserConfirmedResolutionSizeX=1920
LastUserConfirmedResolutionSizeY=1080
DesiredScreenWidth=1920
DesiredScreenHeight=1080
LastUserConfirmedDesiredScreenWidth=1920
LastUserConfirmedDesiredScreenHeight=1080

Make sure the resolution matches your monitor.

Default location:

C:\Users\YOUR_USERNAME\AppData\Local\DeadByDaylight\Saved\Config\WindowsClient\GameUserSettings.ini

------------------------------
3. IMPORTANT
------------------------------

Before editing anything, make a backup of your original files.

Recommended backup files:

Input.ini
GameUserSettings.ini
Engine.ini

To make a backup, simply copy the original files and save them somewhere safe.

Example:

Input.ini.backup
GameUserSettings.ini.backup
Engine.ini.backup

------------------------------
4. OPTIONAL: READ-ONLY
------------------------------

After editing your files, you can set them to read-only to prevent the game from overwriting your settings.

Right-click the file > Properties > Check "Read-only" > Apply.

Warning:
If you set the files to read-only, Dead by Daylight may not be able to save some in-game settings changes anymore.

If you need to change settings in-game later, remove read-only first, launch the game, change your settings, close the game, then re-apply your custom config.

------------------------------
5. SUMMARY
------------------------------

- Add the InputSettings lines to the end of Input.ini.
- Edit your resolution inside GameUserSettings.ini.
- Make sure the resolution matches your monitor.
- Always backup your files before editing.
- Optional: set files to read-only after editing.

------------------------------
6. DBD Overlay Tools
------------------------------

I also created a dedicated overlay app for Dead by Daylight, designed for players, content creators, competitive players, scrims and tournaments.

The app includes many different overlays and tools such as:

- Killer and survivor winstreak overlays
- Copycat streak overlays
- Ladder overlays
- 1v1 timer
- Borrowed Time / Decisive Strike timers
- Hookstage timers
- Tournament overlays
- Scrim tools
- Various custom overlays for Dead by Daylight content and competitive formats

The goal of this app is to make DBD content, streak tracking, competitive sessions and tournaments cleaner, easier to manage, and more professional-looking.

More info here : http://discord.com/invite/aVdT8rRJKc or https://dbdoverlaytools.com/

Best regards,

Steaxs.

