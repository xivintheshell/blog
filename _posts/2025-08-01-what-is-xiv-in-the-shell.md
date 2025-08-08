---
title: What is XIV in the Shell?
date: 2025-08-01 21:13 -0700
author: shanzhe
media_subpath: /assets/01_what_is_xiv_in_the_shell/
---

## Introduction

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hi! I’m shanzhe (Shanzhe Qi @ Seraph), current lead maintainer of XIV in the Shell, a web-based rotation planner for Final Fantasy XIV. I’m starting this blog series because I like writing, and because I want our tool to reach more people in the community. I’ll be making an effort to put out one post every month, but that may change depending on my raiding commitments and general life circumstances.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I’ll be touching on a mix of technical and non-technical Shell-adjacent topics in this series. To lead things off, this post will be answering some burning questions:
1. What is XIV in the Shell?
2. Why XIV in the Shell?
3. What’s next for XIV in the Shell?


## So what is XIV in the Shell?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>XIV in the Shell [https://xivintheshell.com](https://xivintheshell.com) is a web-based FFXIV rotation planner and job simulator.</b>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;That’s it! Most high-end raids in FFXIV have very predictable timelines, and the mechanics of each fight force players to react differently to maintain a coherent rotation. Melees may need to disengage, casters may need to save resources for extended movement, and parties may adjust buff window timings in unconventional ways. Our tool lets you compare a DPS timeline against a fight’s mechanic timeline and party buff windows, and makes precise planning accessible in a way that traditional spreadsheet-based tools do not.

![A screenshot of XIV in the Shell, with fight markers for FRU and opener sequences for BLM, NIN, MNK, and PCT](en_overview.png)
_Some example XIV in the Shell timelines._

### Followup question: who is XIV in the Shell?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nowadays, XIV in the Shell is maintained by a small team of developers as something we work on evenings, weekends, and holidays when we have free time. This site is entirely a passion project, and its features are stable and bug-free enough to generally be quite low-maintenance on a daily basis.


## Why XIV in the Shell?
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Making rotational adaptations on the fly is a valuable skill for raiders to have, but planning while outside instance is useful all the same. Even outside hardcore optimization environments, there are a myriad of reasons to create rotation plans for a fight:
- Theorycrafting sequences for your job
- Getting more comfortable in fights you haven’t yet cleared
- Getting more comfortable in fights you’ve already cleared
- Improving your understanding of a job’s fundamentals
- Moving the colored number on your FFLogs profile up

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Rotation planning can also just be plain fun for its own sake. The interaction between fight mechanics and job kits is a challenging puzzle to solve, and discovering creative solutions then executing them well in-game is a uniquely rewarding experience.

### A Brief History

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Historically, the most prominent tools for rotation planning have been spreadsheet-based. They’re serviceable, flexible, and quite powerful, but are quite cumbersome to use. In Endwalker, miyehn (Ellyn Waterford @ Sargatanas) and UkitaEshiya (Galahad Donnadieu @ Exodus) put together _Black Mage in the Shell_ as essentially a weekend project to support BLM optimization. It spread throughout the BLM community, and by the time I [shanzhe] started raiding in late 6.2, was already quite a mature tool.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Personally, BLM in the Shell’s existence is a large part of why I mained the job throughout Endwalker. By the time I dug my first clear of P8S out of the PF mines in week 31 (the literal day before the tier unlocked!) I had a full GCD-precise plan for phase two of the fight, modified from one that a caster player friend had sent me.

![A screenshot with a sepia filter of an old BLM spell sequence.](hc2.png)
_“Your feeble flame must be snuffed out!”_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Come Dawntrail, I joined a hardcore week 1 prog static for the first time, and during a casual optimization run of M1S in August of 2024, my raid lead (Sterling Sylva @ Goblin) casually remarked:

> You know what would be really cool? If there was a… I mean… for any job obviously…
> …a Picto in the Shell.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Less than 2 weeks later, PCT in the Shell was born. 3 months after that, with several frantic weekends of work and miyehn’s blessing, PCT and BLM were rejoined to create a unified XIV in the Shell. As I write this post in August of 2025, we have extended the site to support all 22 of FFXIV’s combat jobs, and have made significant improvements to the site’s feature set, interface, and performance.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Though I (shanzhe) laid the groundwork for the expansion of BLM in the Shell to supporting rest of the game’s jobs, none of this would have been possible without the support of other developers, particularly miyehn, UkitaEshiya, Akairyu, Sterling, 🐢, Junie, NoHome, and 小铅笔. We’re also indebted to the many members of our communities in The Balance’s Discord and the 不打冰三攻略组 (“Blizzard 3 Skip Strategy Group”) QQ group, who have given invaluable assistance with testing, localizing, and evangelizing our tool.

### Example Use Cases

#### Planning movement with resource generation/consumption

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;You can use XIV in the Shell to precisely sequence resource generation and spending.

_Example:_ Pictomancers can perform an advanced technique known as “magenta skip,” trading a small amount of up-front potency by allowing the Aetherhues buff to expire to increase gauge generation over the course of a fight. XIV in the Shell lets PCTs visualize what spells to cast while waiting for the buff to expire, how those resources align with movement requirements, and whether this extra gauge results in a DPS gain over the course of the fight.

![A sequence of PCT spells.](magenta_skip.png)
_An example Magenta skip in M5S (definitely not optimal, don’t try this at home)_

#### Fitting abilities under a buff window
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;You can use XIV in the Shell visualize how spells fit under party buff and tincture windows, and how they affect potencies.

![A damage table and timeline of a SAM opener.](sam_opener.png)
_Potency report for a standard Samurai opener with slightly staggered buff timings._

#### Checking cooldown usage in a fight with downtime
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fights with extended downtime sequences give players the option to either delay or rush certain cooldowns. While it is possible to figure out whether delaying loses a usage with some math, XIV in the Shell lets you visualize the sequencing of these resources and how tight they are to spend.

_Example:_ Red Mage’s Manafication is on a 110 second cooldown, but requires additional time to complete a melee combo to gain full value. In M7S, a fight with frequent downtime and periods where the RDM is often forced to disengage, XIV in the Shell shows how tight completing the full melee combo sequence is for a strict rush of the ability.

![A timeline with RDM's Manafication and melee combos performed strictly on cooldown.](m7s_manafic.png)
_Barely completing a melee combo from Manafication before the transition to phase 3 of M7S (disclaimer: just an example, not optimal play)._


## What’s next for XIV in the Shell?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nobody works on XIV in the Shell for a living, so the pace of development depends exclusively on our free time and motivation. That said, here’s a few features I’d like to get finished before patch 7.4 rolls around, ordered from least required work to most work:

1. _A better pet damage table._

    Under the hood, we treat pet damage as DoT events with different buff snapshot rules, and they’re displayed as such in potency tables. This can be kind of confusing, and makes it hard to tell how pet damage is broken down.

2. _Better timeline marker selectors._

    The “timeline markers” tab is currently quite cluttered, especially since M8S has varying phase timings to plan around that can change radically depending on a party’s DPS. We also have markers for plenty of older fights that we just don’t have room to cleanly display with the current interface.

3. _Direct skill insertion and an undo button._

    Skills can currently only be inserted at the end of a timeline, and must be manually re-arranged to move an ability usage to an earlier point. There’s also no undo button, so if you accidentally delete a skill with backspace, they have to manually be restored. However, adding direct skill insertion would be a breaking change for users who are used to the current behavior of skills always adding to the end of the timeline, and extra consideration is necessary in determining how best to communicate this change in the UI.

4. _Log import._

    Log import was historically difficult to implement due to limitations in our internal timeline representation. Recent changes have made log import possible, but will still require additional work to infer pre-pull actions that aren’t present in logs and correctly guess a player’s GCD value.

5. _Legacy patch job support._

    From a personal perspective, fantasizing about “how would 6.x BLM’s kit hold up in current savage content?” would be fun, but idle historical interest isn’t the only reason to support older versions of jobs on the site. The CN and KR servers have a delayed patch cycle compared to the global versions of the game; as our current policy is to align with patch changes as quickly as possible, our swift implementation of the 7.2 BLM rework created difficulties for those users. As an interim measure, miyehn created https://xivintheshell.github.io/legacy/ with a snapshot of the site as it was in patch 7.1, but in the future we would like to support significantly reworked jobs directly on the main site to make migration easier.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I don’t have a concrete idea of when we’ll have the time to work on these features, but rest assured these things (and more) are on our radar.

## Conclusion

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Thanks for reading! You can find us on our bsky account [@xivintheshell](https://bsky.app/profile/xivintheshell.com), or on Discord in [#xiv_in_the_shell_support](https://discord.com/channels/277897135515762698/1307922201726685236) in The Balance (you’ll need to grab the “Misc. Support” role). I have a vague idea of what I want the next blog post to be about, but if there’s any topics you’d like us to discuss feel free to let us know.
