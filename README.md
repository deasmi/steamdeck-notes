Steam Deck Notes
================

This is Linux, but it isn't your father/grandfathers Linux. It certainly isn't an Ubuntu/Fedora even proper Arch Linux which it's based on. First major difference, you cannot use the inbuilt package manger (pacman) at all.

All additional software has to be installed as flatpacks.

In a lot of ways this is an appliance like a router running Linux, it has a read only OS, with two versions to allow seamless upgrades and it you leave it alone it'll act like any other console. Turn it on, play games, done.

It does have a desktop mode, but just use it like a Windows/Linux desktop for browser, apps etc. and you are golden.

But.... you can also start fiddling with it and I'll categorise those into two

a) Break the read only seal

b) Don't break the read only seal


Breaking the seal
-----------------

If you break the seal, and it's a single command to do so, you can fiddle with the OS partitions.

These _will not_ survive OS upgrades. Full stop.

I have not done this, this seems like a bad idea, but things like the plugin manager need this at the moment, so I'm not running the plugin manager.


Not breaking the seal
---------------------

If you don't break the seal you can still get into a mess, but it's a local mess, and you won't under any circumstance I can see break the basic gaming functionality of steam. Turn it on in gaming modes and your steam games will work, guaranteed.

So, what can you do ? And how likely to go wrong is it (L/M/H/C(ertain) ?

- Install extra desktop software from the store (L)
- Use it as a desktop, sync your Firefox/chrome settings (L)
- ~~Use Heroic game launcher to install GOG/Epic~~ (M)
  - GOG works well, Witcher 3 and Cyberpunk running OK, but without Steam shaders
  - EPIC is a shit show, well won't run RDR2 and that's all I care about
- ~~Use Lutris to install games/game stores~~ (L)
  - These are self contained in a single directory. You will have one launcher install per game (~200M) so will have to logon separately
  - All wine settings for launcher and game are independent of other games
- EPIC store is rubbish how ever it is installed, at least I cannot get RDR2 to run whatever I do and that's all I have that I care about
- GOG games, download offline installer and run from steam, or just copy folder from PC
- Manually install Origin/GOG/Epic (M/H)
  - See YouTube, rabbit hole, things end up wherever the youtuber thought best.
- Use Boilr to import manual Origin/GOG/Epic games into Steam (L)
- Get steamgrid SGDBOOP working to manage artwork (C)
  - https://github.com/SteamGridDB/SGDBoop/issues/25 - open issue
- Install and run tailscale (M)
  - Jury out, having cloud sync issues, but could be local network issue
- emudeck (L/M)
  - emudeck plays fast and loose with things, and it's a 'please run this random url into bash as root.....' so bad.
  - I will maybe remove and move to RetroDeck
- Steam ROM Manager (L)
  - Nice, works well to add any/all emulators and games to Steam
  - I am only adding Emulation Station and a Few emulators as I don't want 4000 SNES games in Steam
  - I may add Amiga games to steam as they need custom control layouts and I have a nice curated set
- User PATH variable
  - flatpak makes this 'interesting' and by 'interesting' I mean a right royal pain.
  - Who wants to type org.gnu.emacs instead of emacs, because that's how you need to call it.

Amiga Roms
----------

Glob pattern is 
`**/${title}_*@(.adf|.ADF|.adz|.ADZ|.dms|.DMS|.fdi|.FDI|.ipf|.IPF|.hdf|.HDF|.hdz|.HDZ|.lha|.LHA|.slave|.SLAVE|.info|.INFO|.cue|.CUE|.ccd|.CCD|.chd|.CHD|.nrg|.NRG|.mds|.MDS|.iso|.ISO|.uae|.UAE|.m3u|.M3U|.zip|.ZIP|.7z|.7Z)`
