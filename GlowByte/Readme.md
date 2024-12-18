Хакатон GlowByte по тематике автоматизации комплаенса.

Соблюдение законов - это многоуровневый процесс. Банкам жизненно важно узнать какие
операции проводят их клиенты. В случаях, если клиенты банков занимаются финансированием
терроризма, отмыванием доходов или иными нехорошими делами, а банк не пресекает эту
деятельность - банки лишаются лицензий и закрываются.
Через банки ежедневно проходят миллионы операций, которые невозможно проанализировать
вручную. Поэтому для выполнения требований регулятора банком требуется автоматизация таких
проверок.

На этом хакатоне нашей коменде предстояло примерить на себя роль консультантов-экспертов по автоматизации
соблюдения законов. требовалось создать сценарий выявления подозрительных операций, пройдя
по всем шагам, которые Glowbyte проходит в своей работе: 

- Задать уточняющие вопросы бизнес заказчику.

- Написать техническое задание.

- Настроить сценарий выявления в формате sql-запроса и протестировать его.



Формулировка задания.

Настроить сценарий выявления подозрительных операций, код 3612:
Неоднократное внесение одним физическим лицом в течение месяца денежных средств в виде
платы за участие в лотерее, тотализаторе (взаимном пари) и иных основанных на риске играх, в
том числе в электронной форме, в разные розыгрыши на общую сумму, равную или
превышающую 600 000 рублей либо равную сумме в иностранной валюте, эквивалентной 600 000
рублей, или превышающую ее.


# Этап 1 – сбор требований.

На этом этапе мы задавали [вопросы](https://docs.google.com/spreadsheets/d/1tSYBUCYJjk7JT8kDQGpvvVrHPp0aSHZs/edit?usp=sharing&ouid=118407271772589097688&rtpof=true&sd=true) заказчику чтобы в дальнейшем сформировать ТЗ.



# Этап 2 – формирование технического задания (ТЗ)

Далее, основываясь на ответах нам и другим командам(они так же были доступны) мы приступили к составленю [ТЗ](https://github.com/Myxosan/Portfolio/blob/main/GlowByte/ТЗ%20для%20скрипта.pdf).



# Этап 3 – генерация тестовой базы

[База](https://github.com/Myxosan/Portfolio/blob/main/GlowByte/Генерация%20базы.ipynb) сгенерирована с испольозванием Faker и nympy.



# Этап 4 – разработка и тестирование скрипта.

[Скрипт](https://github.com/Myxosan/Portfolio/blob/main/GlowByte/Скрипт.ipynb) написан на sqlite3, он выявляет клиентов (ФЛ — физические лица), участвующих в потенциально подозрительных операциях, основываясь на следующих критериях:

- Частота операций (как минимум 2 транзакции за последние 30 дней).
- Сумма операций (общая сумма превышает 600,000 рублей).
- Специфические шаблоны в назначении платежей (например, ключевые слова, связанные с азартными играми).
- Характеристики клиентов (например, определённые значения okved_code).


# Итоги:
По итогу наша команда заняла 5 место в общем зачете и 2е место по нашему варианту скрипта. [Результаты](https://github.com/Myxosan/Portfolio/blob/main/GlowByte/результаты.jpg) и [Диплом участника](https://github.com/Myxosan/Portfolio/blob/main/GlowByte/Быстров%20Дмитрий.pdf)
