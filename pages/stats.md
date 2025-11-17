---
title: Stats
layout: default
nav_order: 1
---

# Stats
Stats are a list of values that affect how a Yo-kai can interact within the battle. There are several categories of stats:

## Species Base Stats
These stats are base modifiers unique to the *type* of Yo-kai rather than the individual i.e. all Pandles not just any specific Pandle.

| Stat | Notes |
|------|-------|
| BaseA_HP   | |
| BaseB_HP   | |
| BaseA_STR   | |
| BaseB_STR   | |
| BaseA_SPR   | |
| BaseB_SPR   | |
| BaseA_DEF   | |
| BaseB_DEF   | |
| BaseA_SPD   | |
| BaseB_SPD   | |
| AttributeDamageFire   | Fire-elemental attack modifier. |
| AttributeDamageIce    | Ice-elemental attack modifier. |
| AttributeDamageEarth  | Earth-elemental attack modifier. |
| AttributeDamageLightning | Lightning-elemental attack modifier. |
| AttributeDamageWater  | Water-elemental attack modifier. |
| AttributeDamageWind   | Wind-elemental attack modifier. |
| ItemSlots             | Number of items the Yo-kai can equip; Is always a number from 0-2. |
| Money                 | Affects Money dropped when defeated. |
| DropExperience        | Affects Experience points rewarded when defeated. |
| ExperienceCurve       | Scales experience required to level up. |
| CharaRandomActType | |
| BaseLoafAttitude | |

### Modding Info
These can all be edited in charaparam; specifically inside the tree `CHARA_PARAM_INFO` within `romfs:/yw2_a.fa/data/res/character/chara_param_*.cfg.bin`.

## Individual Base Stats
These stats are base modifiers unique to the *Yo-kai itself*.

| Stat |
|------|
| IV_HP   |
| IV_STR  |
| IV_SPR  |
| IV_DEF  |
| IV_SPD  |
| EV_STR  |
| EV_SPR  |
| EV_DEF  |
| EV_SPD  |
| Loaf Attitude |
| Stat Attitude |
| Attitude Points |

### IVs, EVs and Attitudes
IVs are initial values given to a Yo-kai when created. The formula used for legal IVs are `(IV_HP / 2) + IV_STR + IV_SPR + IV_DEF + IV_SPD = 40`. This leads to an interesting side effect where all legal Yo-kai have an even amount of HP IVs.

Auto-befriends have neutral IVs meaning 8 for all stats except HP which is 16 as HP IVs are counted as half in alot of calculations.
The probability for the game to designate **n IVs** for any particular stat has been estimated (not confirmed yet) as follows:

| IV Value       | Probability |
|----------------|------------|
| 0              | 0.013%     |
| 1              | 0.133%     |
| 2              | 0.648%     |
| 3              | 2.052%     |
| 4              | 4.745%     |
| 5              | 8.541%     |
| 6              | 12.456%    |
| 7              | 15.125%    |
| 8              | 15.598%    |
| 9              | 13.865%    |
| 10             | 10.745%    |
| 11             | 7.326%     |
| 12             | 4.426%     |
| 13             | 2.383%     |
| 14             | 1.149%     |
| 15             | 0.498%     |
| 16             | 0.195%     |
| 17             | 0.069%     |
| 18             | 0.022%     |
| 19             | 0.006%     |
| 20             | 0.002%     |
| 21 or more     | 0.001%     |

> **Note:** This distribution is modeled using the following binomial formula:

$$
P(X = n) = \binom{40}{n} \cdot 0.2^n \cdot 0.8^{40-n}
$$

where:  
- `n` is the number of IVs assigned to the stat  
- `40` is the total number of attempts  
- `0.2` is the probability of success per attempt

EVs are effort values which progress in a Yo-kai over time. The total maximum amount of EVs is 20

## Final Core Stats
These are HP, STR, SPR, DEF and SPD:
* HP increases the Player's Max HP
  * Max HP decides the limit and the initial value of the player's Current HP which decides how much damage (after calculations) can be taken before a yokai is "Dead". Dead yokai can be revived mid-battle using Medicine Items and automatically revive after a battle (at 1HP).
  * Current HP can be healed outside of a battle using Food items, Eyepo and Sleeping. During a battle it can be healed via skills, inspirits, souls, and Food items.
* STR affects the damage output of Psychical damage which includes "Attack" attacks and Physical Soultimates.
* SPR affects the damage output of Spiritual damage which includees "Technique" attacks and Spiritual Soultimates.
* DEF lowers the amount of damage taken; this applies to both Physical and Spiritual damage.
* SPD affects turn order and evasion rate. 

