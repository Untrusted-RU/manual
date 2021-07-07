+++
title = "Продвинутая стратегия"
template = "advanced-strategy.html"
+++

{{ heading(text="Продвинутая стратегия") }}

Эта страница посвящена более глубоким стратегиям для победы в игре.
Эта страница в процессе написания, так как игра может сильно изменяться от патча до патча в альфа-стадии.

Внизу вы можете найти руководства по конкретным классам,
или вы можете посетить страницу [Обработка хода в деталях].
Дополнительные советы представлены под списком руководств для классов.

<table style="width: 300px;">
    <tbody>
        <tr>
            {{ strategy_guide(id="NETSEC_OPLEADER", disabled=true)}}
            {{ strategy_guide(id="AGENT_LEADER", disabled=true)}}
            {{ strategy_guide(id="AGENT_FIELD", disabled=true)}}
            {{ strategy_guide(id="AGENT_CONVERTED_FIELDOPS", title="Крот (О/И/Н)", path="mole", disabled=true) }}
            {{ strategy_guide(id="AGENT_RUNAWAY_SNITCH", disabled=true)}}
            {{ strategy_guide(id="NEUTRAL_SCRIPT_KIDDIE", disabled=true)}}
        </tr>
        <tr>
            {{ strategy_guide(id="NEUTRAL_JOURNALIST", disabled=true)}}
            {{ strategy_guide(id="NEUTRAL_RIVAL", disabled=true)}}
            {{ strategy_guide(id="NEUTRAL_BOUNTY_HUNTER", disabled=true)}}
            {{ strategy_guide(id="NEUTRAL_SOCIOPATH", disabled=true)}}
            {{ strategy_guide(id="NEUTRAL_RESENTFUL_CRIMINAL", disabled=true)}}
        </tr>
    </tbody>
</table>

{{ heading(text="Понимание преданности и приоритета") }}

NETSEC players are initially loyal to their faction and all work together towards a common goal – however, most classes can be converted to the AGENT faction.

Most neutral classes do not care about the outcome of the operation as they have their own objective – thus, they could side one way or another depending on how far they are in achieving their goal.

You must always keep in mind who can be your ally: some neutrals classes may be helpful to you early game, but may switch sides at the end for example if they see that AGENTs are gaining power.

Similarly, don’t forget that a NETSEC may be converted to the AGENT faction (unless immune) so always remember that just because someone was loyal on Day 1, that doesn’t mean that he/she is still loyal later on. In facts, agents tend to try to convert someone that is seen as trusted by other players.

As a NETSEC player, try to create a chain of trust by confirming what happened on certain nights (for example, if somone claims to have escorted someone, ask the escortee if indeed somone came to visit him/her) and work your way from there.

As an AGENT, consider even outing one of your allies to gain power and trust.

As a neutral, find out who your allies are and always think of your goal.

Trust no one.

{{ heading(text="Вторичные цели") }}

There are hidden secondary targets throughout the network topology which hold valuable intel – these are called secondary targets and they can yield information which can help NETSEC, and specifically, the effect can be one of the following:

- **Time Extension**: this node holds information that will delay the deadline by 24 hours.
- **Target IP Address**: this node holds information about the IP address of the target.
- **Player Class Type**: this node holds information about the class type of an operative (Offensive, Investigative, Field Ops, Special)
- **Mole Identity**: this node holds information about the identity of a mole (or absence of it)

&zwnj;{{ class(id="NETSEC_SPEARPHISHER") }} and {{ class(id="NETSEC_ANALYST") }} can use their {{ skill(id="DOWNLOAD_INTEL") }} skill on a node to obtain said information.
In order to know for certain that a node holds important information, the aid of an {{ class(id="NETSEC_INSIDEMAN") }} is required via their {{ skill(id="INSIDERKNOWLEDGE") }} skill.
Players can still randomly try to download intel on any node, although that is generally seen suspicious, is absolutely a valid and legitimate operation.
