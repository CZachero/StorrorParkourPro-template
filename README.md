# Overview

This is a guide to get started with map making for STORROR Parkour Pro. There are two ways to use custom maps in the game. The first is to use a mod menu to load your map, which allows you to switch between the official map and custom maps. The second is to replace the game's official main map.

Big shoutout to tarmo888 from whom I forked this repository. tarmo888 created the template for UE 5.5: https://github.com/tarmo888/StorrorParkourPro-template

Another big shoutout to TheMightMage for his Mod Menu and his general work/help in the SPP modding community.

# Prerequisites

Before starting work on a custom map, you will need Unreal Engine installed. Currently, the game uses 5.7, and that is what this guide will be using. In the future, if the game is updated to a later version, this guide will hopefully be updated as well.

Unreal Engine download: https://www.unrealengine.com/en-US/download

You will also need the Windows SDK: https://learn.microsoft.com/en-us/windows/apps/windows-sdk/downloads

If using the mod menu option, you will need Mage's Mod Menu installed: See https://discord.com/channels/789935960904433694/1366173976509812756 or https://www.nexusmods.com/storrorparkourpro/mods/8 for instructions to install. The latest version titled TheMightMages ModMenu UE5.7 publushed on April 7th 2026 is compatible with this guide.

# Download the template

This template contains a couple different branches.

## Using Mod Menu (Recommended)
If you want to use a mod menu to load your map, stay on the main branch and skip to "Download"

## Replacing the main map
If you want to replace the official map with your map, switch to the "replace_map" branch.

<img width="346" height="437" alt="image" src="https://github.com/user-attachments/assets/aec867d2-0ada-4b8e-a7a6-2932e25b6285" />


## Download
Click the green button that says "Code" and select "Download ZIP"

<img width="426" height="370" alt="image" src="https://github.com/user-attachments/assets/7aaab18c-d749-4e55-a827-0f5110d509e6" />

Save the ZIP file in a good location, and extract it.

<img width="788" height="454" alt="image" src="https://github.com/user-attachments/assets/b53b2f4c-12be-4a64-9f39-78677f78747d" />

<img width="611" height="450" alt="image" src="https://github.com/user-attachments/assets/f4de7b95-969d-4809-ab3e-1680be074043" />


## Open the editor

In the folder created by extracting the ZIP file, open `StorrorParkourPro.uproject` with Unreal Editor.

<img width="645" height="354" alt="image" src="https://github.com/user-attachments/assets/cf755e03-5e32-4080-bb5f-93b3d1f7eaa1" />

The editor should look like this:
<img width="2559" height="1390" alt="image" src="https://github.com/user-attachments/assets/0374bc2b-ea95-42e5-8802-6b54facf9108" />
*If there is a black screen instead of the map, double click on Template in the Maps folder to open it*


### Rename your map

If you are using the mod menu, right click on Template in the Maps folder and select Batch Rename:
<img width="1237" height="786" alt="image" src="https://github.com/user-attachments/assets/c7e2688f-2f5c-45d1-b55e-3e4fe4ac7e09" />

In the "Rename To" field, enter your map name and click Apply (NewMap is my example):
<img width="738" height="663" alt="image" src="https://github.com/user-attachments/assets/84e0fd6a-8e7f-41de-9b25-952b4375ae8e" />

*You do not need to enter anything else*

### Start Creating!

Remove the example blockout and build your own.

Open Modeling Mode with Shift+5, and click the Create tab. Try placing some boxes or other shapes.

<img width="780" height="426" alt="image" src="https://github.com/user-attachments/assets/0c39f55f-f90c-4da4-aae5-6ef705b2ad1c" />

<img width="1792" height="1358" alt="image" src="https://github.com/user-attachments/assets/24b5ce94-c37e-48aa-9586-5e4e987e4749" />

Make sure to add collisions to your static meshes! Double click on the image for your static mesh in the Details window:

<img width="1777" height="813" alt="image" src="https://github.com/user-attachments/assets/1ace5dce-05a9-4afe-a1a2-ddf5c4cb0c00" />

You can use box collissions for very simple box shapes:

<img width="1244" height="615" alt="image" src="https://github.com/user-attachments/assets/78404f1e-6ad5-4cba-9669-19dfa95e7fbe" />

Use complex collission as simple for more complicated objects. Click the dropdown for Collission Complexity in the static mesh Details window:

<img width="1941" height="637" alt="image" src="https://github.com/user-attachments/assets/174d772f-f016-4cd0-9801-eafa5aa574b1" />

Don't forget to save!!! There is a spot at the bottom right of the editor that tells you if anything is unsaved.

## Exporting The Mod
In Unreal Editor, click Platforms -> Package Project -> Package Project

Make sure Windows is selected.

<img width="1392" height="768" alt="image" src="https://github.com/user-attachments/assets/f7aca780-6730-483a-9019-e80841f88ced" />

Select `Build` folder inside the project folder and wait for it to finish packaging.

<img width="1022" height="594" alt="image" src="https://github.com/user-attachments/assets/f4c1305d-22c6-442e-a8bc-9d7a1fdf4653" />


## Applying The Mod
* Go to `Build\Windows\StorrorParkourPro\Content\Paks\` folder inside your project folder
* Copy all 3 `pakchunk4564-Windows.*` files to game's `STORRORParkourPRO\Content\Paks` folder, it's in `C:\Program Files (x86)\Steam\steamapps\common\STORROR Parkour Pro\` when installed on Steam
* Rename `pakchunk4564-Windows.*` files to `YourModName_P.*` (`_P` suffix is important)
* It should look like this:

<img width="1020" height="492" alt="image" src="https://github.com/user-attachments/assets/32d150b6-a7b1-4bd1-96a2-bca08c59f26d" />

* Where `pakchunk4564-Windows` can be replaced by your mod's name, and `TheMightMagesModMenu_V5_2_P` is the currently used mod menu. See https://discord.com/channels/789935960904433694/1366173976509812756 or https://www.nexusmods.com/storrorparkourpro/mods/8 for instructions to install. TheMightMages ModMenu UE5.7 from 07 Apr 2026 is currently compatible with the game.
* Open the game via Steam.
* Play the game with your own map if you've replaced the default map.
* If using the mod menu, place a session marker (D-Pad up) and then press ] on your keyboard to open the Mod Menu. Type the name of your map into the bar, and click on the OPEN button (pressing enter on keyboard will not work).

## Distributing The Mod
* Compress those `YourModName_P.*` files (pak, ucas, utoc) into a ZIP file and share it or upload it to Nexus Mods.

