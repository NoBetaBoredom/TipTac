# TipTac
WoW AddOn TipTac

* based on latest version v20.11.04 from Nov 4, 2020
* added fixes for wow patch 9.1.5 (Shadowlands - Chains of Domination)
* added several enhancements

### The following problems are fixed respectively enhancements were added

- lua errors regarding setBackdropColor(), setBackdropBorderColor(), GetRaidTargetIndex() (if icons are enabled), SetPoint()
- background colors
- border colors, also based on unit class or item quality. Additionally the border colors are now "non sticky" if you move your mouse e.g. over items and then over spells.
- backdrop of compare item tooltips, item links and other addons using tiptac to modify tooltips or frames.
- considered new nineslice layout. default tooltip backdrop will be changed with configured backdrop. further styling (background/border texture and backdrop edge size) and 100% solid background is now possible again.
- change between normal and mouse anchors works now while moving your mouse over the corresponding elements.
- prevented flickering of tooltips over buffs if "Anchors->Frame Tip Type" = "Mouse Anchor"
- fixed flickering of tooltip when selecting an item or illusion at transmogrifier if "Anchors->Frame Tip Type" = "Mouse Anchor"
- fixed wrong placement for item comparison tooltips if "Anchors->Frame Tip Type" = "Mouse Anchor".
- added restoring to default font settings when disabling "Font->Modify the GameTooltip Font Templates" without the need to reload the ui for the setting to take effect.
- added styling of tooltips for battle pet, battle pet ability, auras from standard nameplate, auras from addon Plater, DropDownList1/2, FriendsTooltip, LibQTip, LibDBIcon
- changes regarding config option "Special->Enable ChatFrame Hover Hyperlinks":
  - fixed hooking/unhooking of chatframe if toggling option
  - added mouseover for guild/community->chat, battle pets, battle pet abilities, illusions (from Wardrobe)
  - added mouseover for chatlinks: torghast anima power, transmog item/set, azerite essences and dungeon score
- added class border color for member list in guild/community->chat and guild/community->guild roster, dungeon score tooltip and attendees in LFG list if config option "Colors->Color Tip Border by Class Color" is checked
- changes regarding (added) config options under "ItemRef":
  - added border color for spells, unit auras, tradeskills, currencies (in chatframe), achievements, guild challenges (in guild/community->info) and pvp enlistment bonus (in pvp->quick match)
  - added border color and infos for battle pet, battle pet abilities, (world/party) quests in worldmap/questlog/questtracker, questtracker of addon WorldQuestTracker, trade skill reagents (in TradeSkillUI), toys (in ToyBox), items, illusions and sets (in Wardrobe), sets (at Transmogrifier), currencies, achievements in guild/community->info->news, rewards in quest(log)/LFG-browser, azerite essences, runeforge power (in adventure journal), (enhanced) conduits, spells in macros on action bar, torghast anima powers, mini achievement shields in achievement buttons, items/illusions in dress up frame, flyouts (e.g. mage portals), pet actions, keystones (including RewardLevel, WeeklyRewardLevel, ItemID, TimeLimit and AffixInfos)
  - fixed "Smart Icon Appearance" for mounts and mount equipment (in mount journal), items (in adventure journal), spells and items (in guild/community->perks)
- added scroll frame to config options. the scroll bar appears automatically, if content doesn't fit completely on the page.
- applied transparency from standard backdrop and backdrop border to special backdrop and backdrop border
- fixed 1-pixel borders which are sometimes 2 pixels wide
- added icons to item comparison tooltips (ShoppingTooltip1/ShoppingTooltip2 and ItemRefShoppingTooltip1/ItemRefShoppingTooltip2)
- fixed fading issues with tooltip
- fixed hooking tips if event VARIABLES_LOADED from TipTacItemRef fired before the one from TipTac
- fixed sometimes flickering tooltip if moving with flying mount and "Anchors->Frame Tip Type" = "Mouse Anchor"
- added anchors and offsets for ItemRef icon (thx to NoBetaBoredom for PR)
- considered debuff border for aura positions
- splitted options for auras from spells
- classic: fixed lua errors in talents module regarding GetSpecialization() and GetInspectSpecialization()
- classic: added missing styling of auras
- classic: reactivated talent format option
- classic: suppressed error speech/message when calling CanInspect(unit) within TipTacTalents

### The following problems aren't fixed

- Padding for embedded tooltips and battle pet (ability) tooltips doesn't work. However, this only becomes a problem if a particularly thick border is set.

If there are additional fixes in the future, I update this note accordingly.

## Manual Installation

Get [latest release](https://github.com/frozn/TipTac/releases) and replace the folders `TipTac`, `TipTacItemRef`, `TipTacOptions` and `TipTacTalents` with those from the zip file.

Shadowlands: `\World of Warcraft\_retail_\Interface\AddOns`  
Burning Crusade Classic: `\World of Warcraft\_classic_\Interface\AddOns`  
Classic: `\World of Warcraft\_classic_era_\Interface\AddOns`  

## Install with WowUp.io

In WowUp, go to `Get Addons->Install From URL` and enter `https://github.com/frozn/TipTac`
