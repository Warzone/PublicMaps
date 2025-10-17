# Warzone PublicMaps 
<img src="https://warzone.network/img/warzone.svg" align="right" alt="Warzone logo" width="120" height="178"/>

This repository contains public maps and active rotations that are found on [Warzone](https://warzone.network). These maps are designed to be compatible with the [PvP Game Manager (PGM)](https://github.com/PGMDev/PGM) plugin utilzing both Minecraft 1.8.9 as well as the latest version. Non-commercial maps or maps used under the explicit permission of their author(s) are hosted at [PrivateMaps](https://github.com/Warzone/PrivateMaps). For changes, updates, or any other modification intended for privately-hosted maps, please contact a Map Developer on Warzone.
<br/>
<br/>
<br/>

## Contributing

When creating a new map or modifying an existing map, please note some of the requirements for our maps. Pull requests from non-map developers that affect the map rotation are subject to approval and may be closed.

To start contributing, you must clone this repository online, [GitHub Client (recommended for most users)](https://desktop.github.com/), [alternative GUI clients](https://git-scm.com/downloads/guis), or [Git CLI (for advanced users)](https://git-scm.com/) with the command, `git clone https://github.com/Warzone/PublicMaps.git`.

### World Version

-   Every map must work with either Minecraft 1.8.9 or the latest version. To determine the version of a map, you can open the map's `level.dat` with an NBT editor and [find the value of `Data/DataVersion` or `Version`](https://minecraft.wiki/w/Data_version#List_of_data_versions).
-   If the world version is from a different versions of Minecraft outside of 1.8 or the latest, you **must** convert the map to be compatible with one of them.
    -   This can be done with [Chunker](https://github.com/HiveGamesOSS/Chunker) or by using [Mitchell's nbt-converter script](https://github.com/mitchts/nbt-converter).

### Chunk Pruning

In order to remove undesired portions of the map as well as to decrease its total file size, the map needs to be pruned before it can be accepted into the repository.

-   This means that **all** chunks, excluding the map itself, should be deleted from the world.
-   This can be achieved with third-party programs such as [AutoPruner](https://github.com/OvercastCommunity/AutoPruner/releases), [MCASelector](https://github.com/Querz/mcaselector), [MCEdit-Unified](https://github.com/Podshot/MCEdit-Unified), or [MCEdit 2.0](https://github.com/mcedit/mcedit2).
    -   **Note:** PGM Documentation has a [tutorial for chunk pruning](https://pgm.dev/docs/guides/preparing/pruning-chunks).
-   After pruning the map, please make sure that you only include the required world files (`region/*`, `level.dat`, `map.png`, `map.xml`).
    -   For more information about cleaning the world files and preparing the map for publication, [view this page on PGM Documentation](https://pgm.dev/docs/guides/preparing/cleaning-files).

### XML Creation

-   All maps must include a valid `map.xml` to function properly with PGM. The map protocol must be `1.5.0` (older maps are exempt from this requirement).
-   The map version **must** follow the [Semantic Versioning](https://semver.org/) standard.
    -   For example, all new maps will begin at version `1.0.0`. You must increase the version number accordingly with any updates toward that map.
-   Refer to [Additional Resources](#additional-resources) on following proper XML format.

## Support

If you need any additional support with the mapmaking process, you may visit the [#mapmaking](https://warz.one/discord) channel in the Warzone Discord server.

### Additional Resources

-   [PGM Documentation](https://pgm.dev/) - The most current documentation for the latest version of PGM. It covers the various features and modules offered by PGM as well as XML syntax. This resource is useful for beginner mapmakers that are not sure where to begin.
-   [Visual Studio Code](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), or [Notepad++](https://notepad-plus-plus.org/) - Some of the recommended programs for editing XML files, as it comes with syntax highlighting, autocompletion, and other tools to help you create XML files for your maps.
-   [Chunker](https://www.chunker.app/) - an open-source application by Hive Games that can convert Minecraft worlds from a wide range of versions.
-   [webNBT](https://github.com/iRath96/webNBT) or [NBT Explorer](https://github.com/jaquadro/NBTExplorer) - This website will allow you to edit a Minecraft world's level.dat file, which lets you have a control over specific settings not normally present in-game. It can also let you determine what Minecraft version a map was created for.

## License

This repository uses a mixed license model. Unless a map's folder contains a `LICENSE.txt` file specifying otherwise (usually for historical or compatibility reasons), all maps are licensed under the [**CC BY-SA 4.0** license](https://creativecommons.org/licenses/by-sa/4.0/). Therefore, maps without such a file are assumed to follow this default.

Under the default license (CC BY-SA 4.0), you may share, modify, and even use maps commercially, as long as you give appropriate credit and license any modifications under the same terms. By submitting a map intended for Warzone, you agree to follow these terms where applicable.

## Acknowledgements

This repository represents the combined efforts of several contributors, map makers, and map developers since the original release of PGM in 2012 and [TGM](https://github.com/WarzoneMC/tgm) in 2017. Without them, this repository and Warzone would not exist. Additionally, we'd like to credit the following:
-   [MCResourcePile](https://mcresourcepile.github.io/) - for their hard work compiling and archiving hundreds of maps from several communities, making them available for public download and use.
-   Overcast Community's [PublicMaps](https://github.com/OvercastCommunity/PublicMaps) - for their continued efforts in maintaining and updating commercial map files, making them available for everyone.
