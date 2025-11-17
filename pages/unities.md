---
title: Tribe Unities
layout: default
nav_order: 1
---

# Tribe Unities
Tribe Unities are a mechanic that activates mid-battle when 2–3 *adjacent* Yo-kai *of the same tribe** occupy the **front line**.  
They provide buffs to all active allies, with the buff(s) depending on the tribe and the number of adjacent Yo-kai.  

## Base Game Data

| Tribe      | 2 Adjacent Yo-kai | 3 Adjacent Yo-kai | Buff Type                         |
| ---------- | ----------------- | ----------------- | --------------------------------- |
| Brave      | +15%              | +25%              | Strength (STR)                    |
| Mysterious | +15%              | +25%              | Spirit (SPR)                      |
| Tough      | +40%              | +60%              | Defense (DEF)                     |
| Charming   | +10%              | +15%              | Speed (SPD)                       |
| Heartful   | +15%              | +25%              | Healing                           |
| Shady      | +30%              | +60%              | Chance to land negative inspirits |
| Eerie      | +1                | +2                | Inspirit level                    |
| Slippery   | +20%              | +40%              | Chance to dodge enemy inspirits   |

---

## Modding Info
Unity effects can be changed by editing `BTL_FRIEND_BONUS_INFO_LIST` within `romfs:/yw2_a.fa/data/res/battle_config_*.cfg.bin`.
The tree's param is the `ChildCount` if you add a new entry to the tree increase this by 1. The `UnityEffectType`s in YW2 are as follows:
* `1` - Increase STR by primary%
* `2` - Increase SPR by primary%
* `3` - Increase DEF by primary%
* `4` - Increase SPD by primary%
* `5` - Increase healing by primary%
* `6` - Increase odds of landing a negative inspirit by primary%/secondary%?
* `7` - Increase inspirit level by primary
* `8` - Increase odds of dodging enemy inspirits by primary%

## Credits
Credits to aj for discovering this!
