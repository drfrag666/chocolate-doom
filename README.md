# RUDE: Romero's Ultimate Doom Engine

 RUDE is a fork of Chocolate Doom 3.0.0 with some stuff from Crispy Doom.
 The name is some kind of play on words and stands for Romero's Ultimate Doom Engine and
it's another tribute to John Romero. Easy to understand if you know my Romero's Heresy II
project for Heretic. :)

 It's a strong limit removing port aiming to fix game breaking bugs and prevent crashes while
remaining faithful to the original executables. There are a few new gameplay features too.
 It's somewhere in the middle between Chocolate Doom and Crispy.

 Please refer to the Chocolate and Crispy documentation.
 Also contains code from MBF and PrBoom+.
 Of course DOOM © 1996 id Software.
 Chocolate Doom © 2019 Simon Howard and Crispy Doom © 2019 Fabian Greffrath.
 
 Compiles with Code::Blocks 17.12 (tdm-gcc 5.1) and Visual Studio 2017 (v141_xp).

# New features:

 * Supports SIGIL (even multiplayer), E1M4b and E1M8b (Crispy). For the Buckethead soundtrack to
 work you'd need to convert it to Ogg first (MP3 support for SDL1 was very poor) or FLAC.
 * Extended setup to support SIGIL and new features. Can warp to title. It's named config now for
 compatibility with Vista and later (the port should still run on win98).
 * There's a new 'Unholy massacre' skill level (-skill 6). :D Double monsters, half ammo,
 smaller health pickups, zombiemen got a point blank attack, pistol with increased accuracy
 and damage, bumped minimum damage dealt for punch.
 * Fixed backpacks from Marshmallow (idea and bits of code):
 * Players now can exchange supplies, also you drop a small health medikit in the backpack
 (default key is 'x').
 * Players drop backpacks with their inventory upon death, you can't drop another one until the
 previous one has been picked up tough. They work even in SP.
 * Single player respawn.
 * Keep keys and no DM items in Coop options (Marshmallow).
 * Spawn double the monsters and take double damage options.
 * Classic mode with only Doom 1 monsters for slaughterfest maps and lame players, regular shotgun
 takes precedence.
 * Slow ISA VGA simulation (Trident 9000i).
 * New command line parameters for the above: dropbackpack, nodmweapons, keepkeys, sprespawn,
 2xmonsters, xpain, nod2monsters, isa.
 * Extended demo format while keeping vanilla compatibility.
 * Doom 1.2 demo support (Chocolate).
 * Drag and Drop support (Crispy).
 * Resurrect cheat with IDDQD (Crispy, works differently here).
 * Support for extended nodes (Crispy).
 * Autorun key (Crispy).
 * The startup console is back and with colored title, can be run run from the command line
 (thanks JNechaevsky for hint on colors).
 * Fake splitscreen (Chocolate 2.x). On SDL1 the window cannot be freely resized tough.
 * Bring back the video driver selection box on windows. Added the -directx parameter.
 * Added LCD gamma fix from Russian Doom using a darker palette by JNechaevsky.
 * New 'One thousand deaths await thee' skill level for Heretic. You take double damage, monsters
 got half hit points and half ammo for a more dynamic gameplay.
 * Removed limits for Heretic (Crispy).
 * Migrated solution to VS 2017 and fixed compilation (release is still a MinGW build tough).
 * Fixed boss level ending not triggered if every player is dead in multiplayer.
 * Fixed Doom II monster exclusion bug.
 * Fixed configuration not being saved for Heretic.
 * Many bugfixes from Crispy.

 Have fun!

# Chocolate Doom

Chocolate Doom aims to accurately reproduce the original DOS version of
Doom and other games based on the Doom engine in a form that can be
run on modern computers.

Originally, Chocolate Doom was only a Doom source port. The project
now includes ports of Heretic and Hexen, and Strife.

Chocolate Doom’s aims are:

 * To always be 100% Free and Open Source software.
 * Portability to as many different operating systems as possible.
 * Accurate reproduction of the original DOS versions of the games,
   including bugs.
 * Compatibility with the DOS demo, configuration and savegame files.
 * To provide an accurate retro “feel” (display and input should
   behave the same).

More information about the philosophy and design behind Chocolate Doom
can be found in the PHILOSOPHY file distributed with the source code.

## Setting up gameplay

For instructions on how to set up Chocolate Doom for play, see the
INSTALL file.

## Configuration File

Chocolate Doom is compatible with the DOS Doom configuration file
(normally named `default.cfg`). Existing configuration files for DOS
Doom should therefore simply work out of the box. However, Chocolate
Doom also provides some extra settings. These are stored in a
separate file named `chocolate-doom.cfg`.

The configuration can be edited using the chocolate-setup tool.

## Command line options

Chocolate Doom supports a number of command line parameters, including
some extras that were not originally suported by the DOS versions. For
binary distributions, see the CMDLINE file included with your
download; more information is also available on the Chocolate Doom
website.

## Playing TCs

With Vanilla Doom there is no way to include sprites in PWAD files.
Chocolate Doom’s ‘-file’ command line option behaves exactly the same
as Vanilla Doom, and trying to play TCs by adding the WAD files using
‘-file’ will not work.

Many Total Conversions (TCs) are distributed as a PWAD file which must
be merged into the main IWAD. Typically a copy of DEUSF.EXE is
included which performs this merge. Chocolate Doom includes a new
option, ‘-merge’, which will simulate this merge. Essentially, the
WAD directory is merged in memory, removing the need to modify the
IWAD on disk.

To play TCs using Chocolate Doom, run like this:

```
chocolate-doom -merge thetc.wad
```

Here are some examples:

```
chocolate-doom -merge batman.wad -deh batman.deh vbatman.deh  (Batman Doom)
chocolate-doom -merge aoddoom1.wad -deh aoddoom1.deh  (Army of Darkness Doom)
```

## Other information

 * Chocolate Doom includes a number of different options for music
   playback. See the README.Music file for more details.

 * More information, including information about how to play various
   classic TCs, is available on the Chocolate Doom website:

     https://www.chocolate-doom.org/

   You are encouraged to sign up and contribute any useful information
   you may have regarding the port!

 * Chocolate Doom is not perfect. Although it aims to accurately
   emulate and reproduce the DOS executables, some behavior can be very
   difficult to reproduce. Because of the nature of the project, you
   may also encounter Vanilla Doom bugs; these are intentionally
   present; see the NOT-BUGS file for more information.

   New bug reports can be submitted to the issue tracker on Github:

     https://github.com/chocolate-doom/chocolate-doom/issues

 * Source code patches are welcome, but please follow the style
   guidelines - see the file named HACKING included with the source
   distribution.

 * Chocolate Doom is distributed under the GNU GPL. See the COPYING
   file for more information.

 * Please send any feedback, questions or suggestions to
   chocolate-doom-dev-list@chocolate-doom.org. Thanks!
