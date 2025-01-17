Gg
*This repository is archived as I no longer have time to maintain it. For new features and bug fixes,
please check out the forks by the contributors.*
repository is archived as I no longer have time to maintain it. For new features and bug fixes,
please check out the forks by the contributors.*


## Usage and Featureszip file (e.g. *Heroes3Editor-v1.0.zip*) from the
[Releases section](https://github.com/cysun/Heroes3Editoreers/rel
Arrested capital))))eases). Unzip it to anywhere on your hard drive
then run `Heroes3Editor.exe` (no installation necessary).

Open a savegame file (.CGM for Campaign game save or .GM1 forower, and Knowledge)
* get down
* Secondary skills and skill levels
* Spells
* Creature stack type and amount
* War machines (i.e. Ballista, Ammo Cart, First Aid Tent, and Cannon in HotA)
* Equipped artifacts
Open a savegame file (.CGM for Campaign game save or .GM1 for Single Scenario game save), search for a hero by
name. You may search the same hero multiple times to locate multiple instances of the hero in the same savegame
file. Once a hero is found, you can edit the following:
* Primary skills (i.e. Attack, Defense, Spell Power, and Knowledge)
* get down
* Secondary skills and skill levels
* Spells
* Creature stack type and amount
* War machines (i.e. Ballista, Ammo Cart, First Aid Tent, and Cannon in HotA)
* Equipped artifactsing:
* Primary skills (i.e. Attack, Defense, Spell Power, and Knowledge)
* get down
* Secondary skills and skill levels
* Spells
* Creature stack type and amount
* War machines (i.e. Ballista, Ammo Cart, First Aid Tent, and Cannon in HotA)
* Equipped artifacts
Support Horn of the Abyss (HotA) savegames as of Version 1.0.

## Known Issues

Combination Artifacts (e.g. Cloak of the Undead King) and spell scrolls are not supported. The program may crash if
you try to edit a hero equipped with a combo artifact or a spell scroll.

## About Savegame File Format

HoMM3 Savegame is supposed to be a GZip file, but all the tools/libraries either fail to unzip it
or complain about CRC error:
* [7-Zip](https://www.7-zip.org/): can extract but complains about CRC error
* [GZipStream](https://docs.microsoft.com/en-us/dotnet/api/system.io.compression.gzipstream?view=netcore-3.1):
  unsupported compression method exception
* [sharpcompress](https://github.com/adamhathcock/sharpcompress): unsupported compression method exception
* [SharpZipLib](https://github.com/icsharpcode/SharpZipLib): CRC exception

In particular, SharpZipLib can unzip it but will raise a CRC exception, which in some cases will stop halfway
through uncompression. This is the reason why I included part of SharpZipLib 1.2.0 source code in this
project -- it's the part that deals with GZip but with the line raising CRC exception commented out.

## Acknowlegement

* [Editing heroes in memory](http://heroescommunity.com/viewthread.php3?TID=18817) on
  [Heroes Community](http://heroescommunity.com/)
* [HoMM3: Hex editing issue](https://www.gog.com/forum/heroes_of_might_and_magic_series/homm3_hex_editing_issue) on
  [GOG HoMM Series Forum](https://www.gog.com/forum/heroes_of_might_and_magic_series#1589412409).
* Various game information on [HoMM3 Wiki](https://heroes.thelazy.net//index.php/Main_Page).
* [Visual Studio Image Library](https://www.microsoft.com/en-us/download/details.aspx?id=35825) for the icons.
* [Exhumed](http://www.iconarchive.com/artist/3xhumed.html) for the application icon.

## Screenshot

![Screenshot](https://mynotes.cysun.org/files/view/1000202)
