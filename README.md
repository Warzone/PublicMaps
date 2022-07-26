# Warzone PublicMaps 
<img src="https://warzone.network/img/warzone.svg" align="right" alt="Warzone Logo" width="120" height="178">

This repository contains public maps and an active rotation list that are found on [Warzone](https://warz.one). These maps are designed to be compatible with the [PvP Game Manager (PGM)](https://github.com/PGMDev/PGM) plugin and Minecraft 1.8.9. Non-commercial maps or maps used under the explicit permission of their author(s) are hosted at [PrivateMaps](https://github.com/Warzone/PrivateMaps). For changes, updates, or any other modification intended for privately-hosted maps, please contact a Map Developer on Warzone.
<br>
<br>
<br>

## Contributing

When creating a new map or modifying an existing map, please note some of the requirements for our maps. Pull requests from non-map developers that affect the map rotation are subject to approval and may be closed.

To start contributing, you must clone this repository online, [GitHub Client (recommended for most users)](https://desktop.github.com/), [alternative GUI clients](https://git-scm.com/downloads/guis), or [Git CLI (for advanced users)](https://git-scm.com/) with the command, `git clone https://github.com/Warzone/PublicMaps.git`.

### World Version

-   Every map must work with Minecraft 1.8.9. To determine the version of a map, you can open the map's `level.dat` with an NBT editor and [find the value of `Data/DataVersion` or `Version`](https://minecraft.fandom.com/wiki/Data_version#List_of_data_versions).
-   If the world version is from a future (1.9.x and above) or from past (1.7.x and below) versions of Minecraft, you **must** convert the map to be compatible with 1.8.9.
    -   This can be achieved manually or by using [a script to automate](https://github.com/mitchts/nbt-converter) the process.

### Chunk Pruning

In order to remove undesired portions of the map as well as to decrease its total file size, the map needs to be pruned before it can be accepted into the repository.

-   This means that **all** chunks excluding the map itself should be deleted from the world.
-   This can be achieved with third-party programs such as [MCASelector](https://github.com/Querz/mcaselector), [MCEdit-Unified](https://github.com/Podshot/MCEdit-Unified), or [MCEdit 2.0](https://github.com/mcedit/mcedit2).
-   **Note:** When using MCASelector, please make sure you select the `region` folder inside a world folder to edit a world, not the entire world folder.
-   After pruning the map, please make sure that you only include the required world files (`region/*`, `level.dat`, `map.png`, `map.xml`).
    -   For more information about cleaning the world files and preparing the map for publication, [view this page on PGM Documentation](https://pgm.dev/docs/guides/packaging/cleaning-files).

### XML Creation

-   All maps must include a valid `map.xml` to function properly with PGM. The map protocol must be `1.4.0` or above.
-   The map version **must** follow the [Semantic Versioning](https://semver.org/) standard.
    -   For example, all new maps will begin at version `1.0.0`. You must increase the version number accordingly with any updates toward that map.
-   Refer to [Additional Resources](#additional-resources) on following proper XML format.

## Support

If you need any additional support with the mapmaking process, you may visit the [#mapmaking](https://warz.one/discord) channel in the Warzone Discord server.

### Additional Resources

-   [PGM Documentation](https://pgm.dev/) - The most current documentation for the latest (1.8) version of PGM. It covers the various features and modules offered by PGM as well as XML syntax. This resource is useful for beginner mapmakers that are not sure where to begin.
-   [Visual Studio Code](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), or [Notepad++](https://notepad-plus-plus.org/) - Some of the recommended programs for editing XML files, as it comes with syntax highlighting, autocompletion, and other tools to help you create XML files for your maps.
-   [webNBT](https://github.com/iRath96/webNBT) or [NBT Explorer](https://github.com/jaquadro/NBTExplorer) - This will allow you to manipulate any map's `level.dat` as well as determine the version a certain map was created for.

## License

Maps in this repository are made available under the [**CC BY-SA 4.0** license](https://creativecommons.org/licenses/by-sa/4.0/), which allows you to share and adapt any maps of this repository, even for commercial purposes, as long you give appropriate credit and provide your modifications under the same license. By submitting a map for use at Warzone, you agree with the terms of the aforementioned license, and must distribute your map with it where applicable.

## Acknowledgements

This repository represents the combined efforts of PGM contributors, map makers, and map developers since the original release of the plugin. Without them, this repository would not exist. Additionally, we'd like to credit the following:
-   [MCResourcePile](https://mcresourcepile.github.io/) - for their hard work compiling and archiving hundreds of maps from several communities, making them available for public download and use.
-   Overcast Community's [PublicMaps](https://github.com/OvercastCommunity/PublicMaps) - for their continued efforts in maintaining and updating commercial map files, making them available for everyone.
