ZENPROFESSIONS 1.13.0
====================
WoW 3.3.5a / Project Ebonhold

INSTALL
-------
1. Copy the ZenProfessions folder into World of Warcraft/Interface/AddOns/.
2. Keep the bundled UI folder INSIDE ZenProfessions. It is the complete
   ZenStylingPack 1.1.0 and is loaded automatically by ZenProfessions.toc.
   Do not install it as a separate addon.
3. Disable/remove the old EbonholdProfessions folder to prevent duplicate
   launcher buttons and conflicting hotkeys.
4. EbonAPI 2.1+ is OPTIONAL, separately installed, for version alerts ONLY.

STYLING - EMBEDDED ZENSTYLINGPACK
---------------------------------------
- Main profession window, secure profession buttons, settings/blacklist windows,
  item rows, floating launcher and minimap launcher use the bundled Zen styling
  surfaces rather than the previous standalone dark/gold backdrops.
- Fonts, surface palettes, hover highlights and borders follow ZenStylingPack.
- Six live-switchable styles: Classic, Obsidian, Glass, Flat, Brutal, Neon.
- Seven accent presets, fonts, panel opacity and interface scale preferences.
- Open via /zp appearance OR /zp settings > Appearance...
- Appearance preferences are saved under ZenProfessionsDB.appearance and do
  not affect other addons or depend on EbonAPI.

NEW IN 1.13.0 - ZENSTYLINGPACK 1.1.0
----------------------------------------
- All bundled styling-pack code and textures refreshed to the 1.1.0 release.
- Added two native WoW font choices: Morpheus and Skurri. Arial Narrow and
  Blizzard Default remain available.
- Appearance panel uses the v1.1.0 synchronized dropdowns and sliders:
  live controls keep their selected values consistent when themes change.
- Normalization preserves current theme/accent/opacity/scale preferences,
  including the new fonts, in ZenProfessionsDB.appearance.
- ZenStylingPack 1.1.0 also ships optional EbonAPI shared appearance support.
  Its GlobalSync.lua source is bundled but deliberately NOT loaded, because
  ZenProfessions uses EbonAPI ONLY for version announcements. Any prior
  appearance.mode value is set to LOCAL; no global appearance is read/written.

EBONAPI - VERSION UPDATES ONLY
------------------------------
If EbonAPI 2.1+ is installed, ZenProfessions registers its .toc version using
NewAddon(..., {updates=true}). EbonAPI exchanges available addon versions
with other EbonAPI users and can display notices about newer releases.
There is no EbonAPI theme, palette, UI, or settings-page integration.
EbonAPI is NOT required to launch or style ZenProfessions. No files are
updated automatically by EbonAPI's version announcements.

SAVE DATA AND UPGRADES
----------------------
- Keep WTF/Account/<account>/SavedVariables/ZenProfessions.lua when replacing
  1.11.x; all profession hotkeys, blacklists, launchers and sizes are preserved.
- The new appearance settings are stored alongside them in the same DB.
- If upgrading directly from EbonholdProfessions for the first time, exit WoW
  and back up the SavedVariables folder. Copy EbonholdProfessions.lua to
  ZenProfessions.lua. On first login the old EbonholdProfessionsDB table is
  imported as ZenProfessionsDB, if the new DB is not already present.

FEATURES
--------
- Detects learned professions, gathering/tracking and profession abilities
- Secure spell actions and customizable hotkeys
- Optional automatic bag targeting for Prospecting, Milling and Disenchant
- Per-ability item blacklists
- Resizable/movable profession window and independent launcher controls

COMMANDS
--------
/zp                  Toggle professions window
/zp show             Open professions
/zp hide             Close professions
/zp refresh          Rescan professions
/zp debug            Diagnostic chat output
/zp settings         ZenProfessions settings
/zp appearance       Embedded ZenStylingPack appearance editor
/zp style            Alias for appearance
/zp button           Show/hide floating launcher
/zp minimap          Show/hide minimap launcher

Aliases: /zenprofessions, /professions and legacy /ehp.

NOTES
-----
WoW 3.3.5 secure-action behaviour is preserved. Appearance changes are
cosmetic; deferred scale updates are applied after combat if necessary.
No in-game test has been performed; test in the intended WoW client.
