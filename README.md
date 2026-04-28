
# ADVTrains inofficial

 **A bug-fixed build of the ADVTrains mod for Luanti / Minetest.**
  ***What's fixed in this build***

#    Trains now stop at "Stopping point" tracks. The default ARS rule was missing on placement, so trains used to ignore them.
 #   Backwards compatible — existing stop rails in your world also work without re-placing them.
  #  Fixed "stack overflow" crash when enabling the modpack on Luanti 5.14+. The modpack and its inner core mod were both named advtrains, which sent pkgmgr.lua into infinite recursion.
   # Hardened the ATC stop command against missing doors field on legacy stop entries (would otherwise crash the train logic).
  # Stop-rail formspec defaults aligned with placement defaults — "Wait for signal" is now consistently on by default.

### New tool: Auto-Switching Turnout Controller Rail

A new track in the interlocking mod that automatically flips a turnout based on which destination is free.

**    Place the controller rail on the approach side of a turnout.
    Right-click it to set the turnout's position, the two state names (e.g. st / cr), and the TCB on each destination track.
    When a train approaches, the rail checks if the currently-set destination section is occupied. If it is, and the alternate is free, it switches the turnout before the train arrives.
    If both destinations are occupied (or unknown), the turnout is left as-is — no exceptions, no surprises.
    Compatible with ATC, LuaATC, the regular interlocking system, and stop rails (it uses the same setstate API everything else uses).
    Configuration is gated behind the interlocking privilege, just like TCBs and route signals.

Download

Always-fresh ZIP, packaged on the fly from the latest source files on the server(Info: 556 files 11895.4 KB Last change: 2026-04-28 15:23:33).

# How to install

**    Download and unzip the file.
    Locate your Luanti / Minetest mods folder.
    Delete any existing advtrains folder there (important — old files can mask the fixes).
    Copy the advtrains folder from the ZIP into mods.
    Start the game and enable the modpack in your world configuration.
