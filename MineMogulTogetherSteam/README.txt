MineMogul Together (Steam) - BETA
=================================

Drop-in co-op for MineMogul. Play your world together with friends over Steam
(no port-forwarding, no IP sharing) - one player hosts, everyone else joins
straight from a Steam invite. The host's world is the single source of truth;
ore physics, buildings, machines, crates, money, research and quests are all
synced to everyone.

This is a BETA. It works, but you are helping find what breaks. Please report
bugs (see the bottom of this file).


WHAT'S SYNCED
-------------
- Live ore physics (piles, belts, thrown/mined ore) from the host to everyone
- Placing, taking and packing buildings; machines run and animate on clients
- The deposit-box "lift" animation when items are sold
- Purchased crates you can walk up to and collect
- Ore nodes / breakable chunks (host-authoritative mining)
- Shared money, shared research tickets, shared "For Sale" area unlocks
- Shared quest progress
- Other players shown as moving avatars with their Steam name
Each player keeps their OWN inventory and tools; money and research are shared.


REQUIREMENTS
------------
1. BepInEx 5 (x64) installed in your MineMogul folder.
   - If you don't have it: download BepInEx 5 x64, extract it into your
     MineMogul game folder, then run the game ONCE so it creates its folders.
   - After that first launch you should have a BepInEx\plugins\ folder.
2. Steam running and logged in, on an account that owns MineMogul.
3. Everyone playing together must be Steam friends.


INSTALL
-------
Extract this zip and drop the "MineMogulTogetherSteam" FOLDER into:

    ...\steamapps\common\MineMogul\BepInEx\plugins\

so it looks like:

    BepInEx\
      plugins\
        MineMogulTogetherSteam\
          MineMogulTogetherSteam.dll
          Facepunch.Steamworks.Win64.dll
          steam_api64.dll
          steam_appid.txt

That's it. Launch the game. If BepInEx is set up correctly the mod loads
automatically.

Updating: delete the old MineMogulTogetherSteam folder from plugins\ first, then
drop in the new one (so you don't run two copies at once). Do NOT run this at the
same time as the old UDP "MineMogulTogether.dll" build - remove that if present.


HOW TO PLAY
-----------
Press F6 in game to open the Together panel (it works from the main menu too).

HOST:
  1. Load your save (or start a New Game), then click "Host Game".
  2. Click "Invite Friends" to open the Steam overlay and invite people,
     or share the SteamID shown in the panel.

JOIN:
  - Accept the Steam invite, or click "Join Game" on the host's Steam profile,
  - or paste the host's SteamID64 into the "Host ID" field and click Join.
  The host's world loads automatically - you don't need to be in a world first.

Keys:  F2 host  -  F3 join  -  F4 disconnect  -  F6 open/hide panel
(The panel starts hidden - press F6 to open it.)


KNOWN LIMITATIONS (BETA)
------------------------
- The Steam overlay must be enabled (Steam > Settings > In Game) for the
  "Invite Friends" button and profile "Join Game" to work. Pasting a SteamID
  works regardless.
- Explosion/particle effects for area unlocks are shown on the host only; the
  wall still opens for everyone.
- High object counts (very large ore piles) increase the host's bandwidth/CPU.
- Some machine or effect edge cases may not replicate perfectly yet - that's
  exactly the kind of thing this beta is for.


REPORTING BUGS
--------------
When something breaks, note what you were doing and grab these files if you can:
  BepInEx\LogOutput.log
  TogetherLogs\  (per-session net logs)
The in-game panel also shows live connection stats (RTT / bandwidth / object
count) that are useful to mention.


Made by CelestialTree.
