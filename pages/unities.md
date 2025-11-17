---
title: Tribe Unities
layout: home
nav_order: 1
---

# Tribe Unities

## Explanation and Data
Tribe Unities are a mechanic that occurs mid-battle when there are 2-3 adjacent yokai which share the same tribe and are within the front line. Based on the amount of adjacent Yo-kai (2/3) and the Tribe different buffs will be applied to the active allies. The buffs in the unmodified game are as follows:
Brave: +15%/+25% of strength 
Mysterious:+15%/+25% of spirit
Tough: +40%/+60% of defense
Charming:+10%/+15% of speed
Heartful:+15%/+25% of healing
Shady:+30%/+60% of hitting negative inspirits 
Eerie:+1/+2 levels in inspirits
Slippery:+20%/40% of avoiding enemies' inspirits.

## Modding Info
These can be changed in a mod by editing `BTL_FRIEND_BONUS_INFO_LIST` in `yw2_a.fa/data/res/battle_config_*.cfg.bin`, where the `UnityEffectType`s in Yo-kai Watch 2 are:
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
