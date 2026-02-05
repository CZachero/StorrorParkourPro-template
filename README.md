# Template for modding STORROR Parkour Pro
This is a template for modding STORROR Parkour Pro main open-world map. It has all the changes done to get started with your own map, so you can easily just package the *.pak patch files to override the main map.

## Getting Started
* Download & Install Unreal Engine 5.6.* https://www.unrealengine.com/en-US/download
* Download this template (Code -> Download ZIP)
* Open `StorrorParkourPro.uproject` with Unreal Editor
* Remove the example blockout and build your own

## Exporting The Mod
* In Unreal Editor, click Platforms -> Windows -> Package Project
* Select `Build` folder inside the project folder

## Applying The Mod
* Go to `Build\Windows\StorrorParkourPro\Content\Paks\` folder inside your project folder
* Copy `pakchunk4564-Windows.*` files to game's `STORRORParkourPRO\Content\Paks` folder, it's in `C:\Program Files (x86)\Steam\steamapps\common\STORROR Parkour Pro\` when installed on Steam
* Rename `pakchunk4564-Windows.*` files to `YourModName_P.*` (`_P` suffix is important)
* Play the game with your own map

## Distributing The Mod
* Compress those `YourModName_P.*` files (pak, ucas, utoc) into a ZIP file
