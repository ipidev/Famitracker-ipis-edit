# Famitracker - ipi's edit
This fork of FamiTracker 0.4.2 dates back to 9th January 2014. I had decided to add some features which I personally found useful, such as the Lxx effect and the multiple expansion chip selector. These changes apparently inspired the creation of HertzDevil's well-known [0CC-Famitracker](https://github.com/HertzDevil/0CC-FamiTracker) fork, which has had many new features added since.

While this version of FamiTracker is now largely outdated (and indeed never really got a proper name), I've decided to publish it to ensure this piece of chiptune history is not lost. 0CC-Famitracker is a tool that many people use and enjoy, and it's nice to have at least had a small part in its development.

Examples of code changes can be found in ChannelHandler.cpp (unfortunately not marked - try seraching for `m_iNoteRelease`).

Useful links.
- [FamiTracker's website](http://famitracker.com)
- [The discussion thread on the FamiTracker forums](http://famitracker.com/forum/posts.php?id=5235)
- [A built executable version (provided as-is)](http://ipidev.info/junk/famitracker/Famitrackeripi_r2.zip)

The original FamiTracker source code and this fork are liscenced under GPL v2 - see GPL.txt.

## Changelog

What follows is the contents of changelog.txt that are relevant to the changes I made (note the published version is "r2").

##### Version 0.4.2, ipi's edit r2

Known bugs:
- EEx has no effect on VRC7 channels.

Fixed bugs:
- Fixed a bug where Hxx/Ixx on FDS became out of sync.
- Fixed a bug when using different arps speeds with a 0x0 effect.
- Using 0x0 arpeggios now acts like it does in FT 0.4.2.
- Fixed a bug where channel volume and the volume column were ignored for instruments with blank volume envelopes.

##### Version 0.4.2, ipi's edit

New stuff:
- Added the Lxx delayed release effect - similarly to Sxx, it releases the current note after xx ticks.
- Completely changed Exx - it is now the extra effect (similar to XM's Exx).
  - E0x sets the frequency of arpeggios in ticks. E00 will stop arpeggios.
  - EEx sets the channel's volume to x. EE0 will mute the channel.
- The module properties window now allows you to choose multiple expansions.

Known bugs:
- Instruments with no volume envelope are unaffected by EEx.
- Sunsoft B5 implementation is very unfinished (and should not be used).

Fixed bugs:
- Fixed a bug where VRC7/B5 channels were being removed by having less than 8 N163 channels.
- Fixed a "bug" where saving B5 modules was not allowed.

To add:
- More Exx effects, maybe vibrato envelope, glissando?
- The ability emulate older VRC7 patches (and possibly blank volume envelope behaviour).
- NSF export for the added effects.
- NSF export for multichip... but this is unrealistic.

Not going to be added:
- B5 export.
- Multiplexing control.
