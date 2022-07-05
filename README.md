# Folkwang

An own custom Minecraft modpack based on [Valhelsia 3](https://github.com/ValhelsiaTeam/Valhelsia-3).
It focus on an relaxed playstyle for different interests.

* Want to do some bloody magic or communicate with elfs to get mystical flowers?
* Suit yourself up and fight the bosses of the twilight forest.
* Build a powerfull reactor and automate all of your daily tasks.
* Explore several biomes in several worlds, to find a nice place to stay.
* Simply build yourself a nice and cozy home to live in.

What will it be for you? Find out for yourself.

## Included mods

For a list of included mods take a look in the [mods list](https://poeschl.github.io/Folkwang/mods.txt).
It gets automatically updated on each version.

## Voice Mod

In the pack the Simple Voice Chat mod is included. That means Voice chatting without any service like TS3 or Discord is possible.

Per default its voice-activated but muted, to change the settings press `.` while in game to change any voice related settings.
That way nobody can hear you until you enable it.s

## Use this pack

### PolyMC

The recommended way of launching this modpack is with [PolyMC](https://polymc.org/).
It allows to play modpacks from several big modpack plattforms and does not track any usage of it.

With this way you are always automatically up-to-date with the latest files of Folkwang.
They will be updated on every start of the modpack.

The import is done via the "Add instance" button on the top left of PolyMC, then choose "Import from zip file" and enter
the following url:

```txt
https://poeschl.github.io/Folkwang/Folkwang-rolling.zip
```

PolyMC will now download the needed metadata and will install all mods on the first start.
*Make sure the modpack has more then 4GB of memory available.* If not, see 
[this help](https://github.com/MultiMC/Launcher/wiki/Increasing-Java's-memory-allocation).

### Curseforge

If you want to use Curseforge to get the modpack, browse to [Folkwang](https://www.curseforge.com/minecraft/modpacks/folkwang)
or search in the Curseforge Launcher for "Folkwang".

Make sure to look out for updates, since its not updating for itself (I think).

## Server-Version

The Folkwang pack uses [Minecraft Forge 36.2.35](https://files.minecraftforge.net/net/minecraftforge/forge/index_1.16.5.html),
please download the forge installer and install an Forge Server by executing the installer to an path of your liking.

After that download the [packwiz-installer-bootstrap](https://github.com/packwiz/packwiz-installer-bootstrap/releases)
jar file and put it inside the folder where the `forge-1.16.5-36.2.35.jar` is located. Execute it afterwards following command.

```shell
# Download all pack resources
java -jar packwiz-installer-bootstrap.jar -s server https://poeschl.github.io/Folkwang/pack.toml
```

It will download all needed modfiles and configs let you start your server easily.
The recommended requirements for running a server is 6 GB of memory and Java 11.
For starting I use following command for my server.

```shell
java -jar -Xmx6G \
  -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 \
  forge-1.16.5-36.2.35.jar nogui

```

## Building packs manually

To create a CurseForge / PolyMC compatible modpack the software [packwiz](https://packwiz.infra.link/) is used.
It need to be installed on the system which creates the final pack.

After installing the client and server pack can be build by running

```shell
# Client pack
packwiz curseforge export --side client

# Server
packwiz curseforge export --side server
```

## About the name

`Fólkvangr` was a meadow or field ruled over by the goddness Freyja in the nords mythology.
[Wikipedia](https://en.wikipedia.org/wiki/F%C3%B3lkvangr)

