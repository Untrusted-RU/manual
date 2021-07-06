+++
title = "NETSEC"
weight = 0

[extra]
id = "NETSEC"
image = "1_faction_netsec"
win_condition = """\
Взломать целевой узел. \
Если у нас получится, даже если нас арестуют - мы точно выберемся из тюрьмы, \
учитывая, кто наш клиент...\
"""
members = [
    "NETSEC_OPLEADER",
    "NETSEC_CCTV_SPECIALIST",
    "NETSEC_NETWORK_SPECIALIST",
    "NETSEC_BLACKHAT",
    "NETSEC_SOCIAL_ENGINEER",
    "NETSEC_INSIDEMAN",
    "NETSEC_SPEARPHISHER",
    "NETSEC_ENFORCER",
    "NETSEC_ANALYST",
    "NETSEC_IMPROVISED_HACKER",
]
+++

**NETSEC** - команда хакеров, собранная неизвестным гением.
Их цель - получить доступ к определённому серверу в данной сети.
Никто не знает их предыдущих методов,
являются ли они обыкновенными преступниками,
или преследуют более высокую цель.
По правде говоря, их методы часто крайне незаконны,
если не аморальны вовсе.

**Условия победы**:
игра заканчивается, когда NETSEC получают доступ к целевому узлу, или когда все члены AGENT убраны из игры.
