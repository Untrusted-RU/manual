+++
title = "Основные правила"
+++

{{ heading(text="Цель игры") }}

В Untrusted, две основные [фракции](/factions) противостоят друг другу,
и любой член каждой фракции может победить, если его фракция победит в конце игры
(бонусные очки для разблокировки новых аватаров начисляются тем, кто остался в живых).

Игроки из [NETSEC](/factions/#NETSEC) могут выиграть путём взлома определённого компьютера (узла) в сети (также называемого целевым узлом)
или путём устранения всех членов AGENT.

Игроки из [AGENT](/factions/#AGENT) могут выиграть, убрав из игры всех членов NETSEC,
или получив {{ skill(id="GRANT_ROOT", text="рут-права")}} от Лидера операции.

Нейтральные классы преследуют собственные цели, и могут выбрать сторону как NETSEC, так и AGENT, если захотят.

Вне зависимости от назначенного вам класса, каждый игрок следует общему процессу игры до самого её конца.

{{ heading (text="Игровой процесс") }}

Процесс игры в Untrusted основан на цикле дня и ночи –
каждый день и каждую ночь вы можете совершить одно из доступных действий для вашего класса.

В зависимости от числа игроков в матче (также называемого OPSEC), игра длится определённое количество дней:
к примеру, в OPSEC из 10 игроков, цель должна быть взломана за 7 дней.
Некоторые навыки (на данный момент, только {{ skill(id="DOWNLOAD_INTEL", suffix=")") }} могут увеличить доступное время.

В течении дня, большинство навыков сфокусированы на взломе целевой сети, или, другими словами, взаимодействуют с узлами в сети.

В течении ночи, большинство навыков сфокусированы на исследовании других игроков, или предотвращении такого исследования.

Каждый день или ночь также можно проголосовать за устранение игрока.

После каждого дня и ночи, сводка событий отображается каждому игроку. Одни события видны только вам, а другие - всем.
Untrusted немного отличается от похожих игр такого жанра: если вы встретитесь с кем-то, то будете знать, кто это был.
Если вам заплатили за установку и возврат кейлоггеров для NETSEC ({{ class(id="NETSEC_INSIDEMAN", suffix=")") }}, имеет смысл рассказать об этом всем учасникам взлома.
Всегда контролируйте происходящее и сверяйте с тем, что остальные говорили ранее
(вы можете кликнуть на любое имя в чате, чтобы открыть историю их сообщений).

{{ heading(text="Взлом сети") }}

Топология сети - сетка 3 строки на 4 колонки (для игр на 10 человек) и может достигать 3×5 или 4×5 с возрастанием числа игроков.
В начале игры NETSEC видят только входные узлы (в первой колонке) и смогут увидеть остальные узлы только после взлома
и получения доступа к видимым узлам. Не все узлы гарантированно подключены прямым путём к целевому узлу.

AGENT видят всю сеть с самого начала игры, поэтому им стоит планировать свою стратегию в соответствии с созданной топологией сети
(обратив особое внимание на потенциальные критические точки).

<table>
    <tr>
        <td><img
                    loading="lazy"
                    src="https://i2.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_topology.png?resize=311%2C245&amp;ssl=1"
                    alt="" width="311" height="245"
                    class="aligncenter size-full wp-image-271"
                    srcset="https://i2.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_topology.png?w=311&amp;ssl=1 311w, https://i2.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_topology.png?resize=300%2C236&amp;ssl=1 300w, https://i2.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_topology.png?resize=250%2C197&amp;ssl=1 250w, https://i2.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_topology.png?resize=228%2C180&amp;ssl=1 228w"
                    sizes="(max-width: 311px) 100vw, 311px"
                    data-recalc-dims="1" /></td>
        <td>

Целевой узел помечет тремя красными кругами, и всегда находится на 4 колонке.

Взломанные узлы помечены зелёным цветом, а пока не взломанные - белым.

Соединение (линия между двумя узлами) означает, что эти компьютеры соединены между собой,
и это позволяет видеть и подключаться ко всем соединённым с данным узлом компьютерам.
Вам необходим прямой путь от входной точки до целевого узла для того, чтобы его взломать.

</td></tr></table>

Обратите внимание, что каждый узёл создаётся независимо от остальных – это означает,
что взлом одного ноутбука может быть труднее или легче другого, но сервера всегда труднее для взлома, чем ноутбуки.
Характеристики каждого узла определяются в начале игры, и их “сложность взлома” может быть изменена разными навыками в процессе игры.
Такие изменения (к примеру, использование {{ skill(id="SPEARPHISH_EXECUTION") }}
или других навыков для увеличения/уменьшения сложности взлома) постоянны и сочетаются друг с другом –
координируйте их использование с командой для максимального шанса на успех!

AGENT знают топологию сети, а все остальные видят только входные узлы (первая колонка).
Когда NETSEC взламывают узел, все узлы, напрямую соединённые с ним, становятся видны.
AGENT также знают, какой узел является Целевым Узлом (помечен красной иконкой)

&zwnj;{{ class(id="NETSEC_INSIDEMAN", text="Свои люди") }} знают целевой узел и увидят иконку цели, как только NETSEC взломает узел, напрямую подключенный к нему.
Впрочем, NETSEC также могут использовать навык {{ skill(id="DOWNLOAD_INTEL") }} и получить шанс узнать IP-адрес целевого узла.

Как и в реальной жизни, нет никакой гарантии, что вы сможете взломать выбранный узел.
Некоторые классы более опытны во взломе, чем другие, и имеют больше шансов взломать свою цель.
Классы, имеющие навыки взлома, в порядке от более опытных до менее опытных: {{ class(id="NETSEC_BLACKHAT", suffix=",")}} {{ class(id="NETSEC_NETWORK_SPECIALIST", suffix=",") }} {{ class(id="NETSEC_OPLEADER", suffix=",") }} {{ class(id="NETSEC_SOCIAL_ENGINEER", suffix=",") }} {{ class(id="NETSEC_SPEARPHISHER", suffix=",") }} {{ class(id="NETSEC_IMPROVISED_HACKER", suffix=".") }}

<table style="width:100%;">
    <tr>
        <td style="width:100px;margin:auto;text-align:center;">
            <img
                loading="lazy"
                src="https://i2.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_laptop.png?resize=81%2C58&amp;ssl=1"
                alt="" width="81" height="58" class="alignnone size-full wp-image-266"
                data-recalc-dims="1" />
        </td>
        <td style="text-align:justify;border:0px;">
            <u>Ноутбуки</u><br />
            Узлы с этой иконкой - ноутбуки, их проще взломать.<br />
            Ноутбуки могут появляться в 1-ой, 2-ой и 3-ей колонках топологии сети.
        </td>
    </tr>
    <tr>
        <td style="width:100px;margin:auto;text-align:center;border:0px;">
            <img
                loading="lazy"
                src="https://i1.wp.com/www.playuntrusted.com/wp-content/uploads/2020/04/untrusted_server.png?resize=62%2C57&amp;ssl=1"
                alt="" width="62" height="57" class="alignnone size-full wp-image-267"
                data-recalc-dims="1" />
        </td>
        <td style="text-align:justify;">
            <u>Сервера</u><br />
            Узлы с этой иконкой - сервера, их тяжелее взломать.<br />
            Сервера могут появляться во 2-ой, 3-ей и 4-ой колонках топологии сети.
        </td>
    </tr>
</table>

Клик на любой взломанный (зелёный) узел отобразит логи подключения к нему - список, показывающий, кто и когда подключался к данному узлу. Будьте осторожны - некоторые навыки ({{ skill(id="ROLLBACK", suffix=",") }} {{ skill(id="ALTER_LOGS", suffix=")")}} могут подделать эту информацию. {{ class(id="NETSEC_ANALYST") }} тут особенно полезен, так как он может использовать {{ skill(id="LOG_ANALYSIS", suffix=",")}} чтобы убрать все поддельные логи с любого (взломанного) узла.

{{ heading(text="Основной геймплей") }}

В зависимости от вашего класса способ игры будет отличаться, но есть определённые вещи, которые всегда стоит делать:

- Убедитесь, что записываете свои действия в ваш Персональный лог
- Создайте круг доверия с остальными игроками на основании их слов и действий
- Проверьте лог арестованного/мёртвого игрока как можно раньше
- Координируйте действия с другими игроками. Информация - ключ к победе.

{{ heading(text="Базовая стратегия - NETSEC") }}

Если вы начали игру за класс из NETSEC, первым делом убедитесь, что знаете ключевые обязанности вашей роли.
Нажмите F1, чтобы свериться с руководством в игре.

- Классы-нападающие ({{ class(id="NETSEC_BLACKHAT", suffix=",") }} {{ class(id="NETSEC_SPEARPHISHER", suffix=",")}} {{ class(id="NETSEC_IMPROVISED_HACKER", suffix=")") }} сильны в быстром взломе узлов
- Классы-исследователи ({{ class(id="NETSEC_SOCIAL_ENGINEER", suffix=",") }} {{ class(id="NETSEC_NETWORK_SPECIALIST", suffix=",") }} {{ class(id="NETSEC_ANALYST", suffix=")") }} сильны в исследовании сети
- Классы-оперативники ({{ class(id="NETSEC_INSIDEMAN", suffix=",") }} {{ class(id="NETSEC_CCTV_SPECIALIST", suffix=",") }} {{ class(id="NETSEC_ENFORCER", suffix=")") }} сильны в исследовании других игроков

&zwnj;{{ class(id="NETSEC_OPLEADER") }} - критически важный класс для NETSEC:
кроме того, что это единственный класс, обладающий мощным навыком {{ skill(id="ZERODAY_EXPLOIT", suffix=",") }} 
{{ class(id="NETSEC_OPLEADER", link=false) }} - единственный, кто может анонимно рассылать сообщения всем игрокам (включая членов AGENT).
Следовательно, {{ class(id="NETSEC_OPLEADER", link=false) }} должен координировать действия NETSEC.

<u>Открыто заявлять свою роль в Untrusted очень опасно:</u> хороший {{ class(id="NETSEC_OPLEADER", link=false) }} спрашивает о ролях и логах по возможности анонимно, так как подтверждённый член NETSEC почти наверняка станет целью №1 для AGENT.

{{ heading(text="Базовая стратегия - AGENT") }}

Сила AGENT - в доступной им информации: они знают своих членов и топологию сети с самого начала игры.
Тем не менее, их ресурсы ограничены, а действия требуют большой осторожности.
Потеря таких классов, как {{ class(id="AGENT_FIELD") }} или {{ class(id="AGENT_LEADER") }} на ранней стадии игры очень упростит жизнь NETSEC.

- Тихие игроки более подозрительны: старайтесь участвовать в обсуждениях в основном чате,
  сейте сомнения касательно других игроков, не привлекая к себе излишнего внимания
- Убедитесь, что подделываете убедительные логи: достаточно одной неверной записи, чтобы вас раскрыли и убили.
- &zwnj;{{ class(id="AGENT_LEADER", link=false) }} может использовать навык {{ skill(id="STRIKE_DEAL") }} и превратить до двух игроков в игре в кротов ({{ class(id="AGENT_CONVERTED_FIELDOPS", suffix=",") }} {{ class(id="AGENT_CONVERTED_INVESTIGATIVE", suffix=",") }} {{ class(id="AGENT_CONVERTED_OFFENSIVE", suffix="):") }}
  их голос, безусловно, важен, но не бойтесь использовать их как козлов отпущения (в открытую обвиняя их),
  чтобы, по необходимости, заслужить доверие и выиграть себе время.
- По возможности используйте критические точки в топологии сети для замедления прогресса NETSEC.
  Обратите внимание, что навык {{ skill(id="DENIAL_OF_SERVICE") }} может предотвратить использование навыков {{ skill(id="ROLLBACK") }} и {{ skill(id="ALTER_LOGS", suffix=".")}}

{{ heading(text="Базовая стратегия - Нейтральные классы") }}

Игра за каждый нейтральный класс отличается от игры за другой –
хоть некоторые классы могут стать на сторону как NETSEC, так и AGENT, в конце концов только вам решать, как вы хотите играть.
Сверьтесь с внутриигровым руководством (F1) для информации о вашем классе.
