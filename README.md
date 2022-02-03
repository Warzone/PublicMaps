# Warzone PublicMaps

This repository contains public maps and active rotation list that are found on [Warzone](https://warz.one). These maps are designed to be compatible with the [PvP Game Manager (PGM)](https://github.com/PGMDev/PGM) plugin and Minecraft 1.8.9.

## Contributing
When creating a new map or modifying an existing map, please note some of the requirements for our maps. Pull requests from non-map developers that affect the map rotation are subject to approval and may be closed.

### World Version
* Every map must work with Minecraft 1.8.9. To determine the version of the map, you can load it into your Singleplayer Menu.
* If the world version is from a future (1.9.x and above) or from past (1.7.x and below) versions of Minecraft, you **must** convert the map to be compatible with 1.8.9.
  * This can be achieved manually or by using [a script to automate](https://github.com/mitchts/nbt-converter) the process.

### Chunk Pruning
In order to remove undesired portions of the map as well as to decrease its total file size, the map needs to be pruned in order for it to be accepted into the repository.
* This means that **all** chunks excluding the map itself should be deleted from the world.
* This can be achieved with third-party programs such as [MCASelector](https://github.com/Querz/mcaselector), [MCEdit-Unified](https://github.com/Podshot/MCEdit-Unified), or [MCEdit 2.0](https://github.com/mcedit/mcedit2).
  * **Note:** When using MCASelector, please make sure you select the `region` folder inside a world folder to edit a world, not the entire world folder.
* After pruning the map, please make sure that you only include the required world files (`region/*`, `level.dat`, `map.png`, `map.xml`, ). 
  * For more information about cleaning the world files, [view this page on PGM Documentation](https://pgm.dev/docs/guides/packaging/cleaning-files).

### XML Creation
* All maps must include a valid `map.xml` to function properly with PGM. The map protocol must be `1.4.0` or above.
* The map version **must** follow the [Semantic Versioning](https://semver.org/) standard.
* Refer to [Additional Resources](#additional-resources) on following proper XML format.

## Support
If you need any additional support with the mapmaking process, you may visit the [#mapmaking channel in the Warzone Discord server](https://warz.one/discord).

### Additional Resources
* [PGM Documentation](https://pgm.dev/) - The most current documentation for the latest (1.8) version of PGM. It covers the various modules as well as XML syntax. This resource is useful for beginner mapmakers that are not sure where to begin.
* [OCN XML Documentation](https://docs.oc.tc/) - Older, but readable, documentation which contains some modules from 1.9.x PGM. Some contents covered here may not work with the 1.8 fork of PGM used by Warzone.
* [Visual Studio Code](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), or [Notepad++](https://notepad-plus-plus.org/) - Some of the recommended programs for editing XML, as it comes with syntax highlighting, autocompletion, and other tools to help you create XML files for your maps.

## License
Maps in this repository are made available under the [**CC BY-SA 4.0** license](https://creativecommons.org/licenses/by-sa/4.0/), which allows you to share and adapt any maps of this repository, even for commercial purposes, as long you give appropriate credit and provide your modifications under the same license. By submitting a map for use at Warzone, you agree with the terms of the aforementioned license, and must distribute your map with it where applicable.

## Acknowledgements
This repository represents the years of efforts made by Warzone staff, map developers, and contributors. Without them, none of this would have been possible. Kudos to them for their great work maintaining Warzone's maps.
