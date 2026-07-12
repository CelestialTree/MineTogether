# MineMogul Together (Steam) - Beta download

Drop-in co-op for [MineMogul](https://store.steampowered.com/app/3846120/MineMogul/).
Play your world together over Steam - one player hosts, everyone else joins from a
Steam invite. No port-forwarding, no IP sharing.

This branch is the **ready-to-use build**. The source lives on the [`dev`](../../tree/dev) branch.

## Install

1. Install **BepInEx 5 (x64)** into your MineMogul folder and run the game once so it
   creates `BepInEx\plugins\` (see the folder's `README.txt` for details).
2. Download this branch (green **Code** button -> **Download ZIP**).
3. Drop the **`MineMogulTogetherSteam`** folder into:

   ```
   ...\steamapps\common\MineMogul\BepInEx\plugins\
   ```

4. Launch the game and press **F6** to open the Together panel.

Full instructions, controls, requirements and known limitations are in
[`MineMogulTogetherSteam/README.txt`](MineMogulTogetherSteam/README.txt).

Updating: delete the old `MineMogulTogetherSteam` folder from `plugins\` before dropping
in the new one.

---

This is a **beta** - please report anything that breaks. Made by CelestialTree.
