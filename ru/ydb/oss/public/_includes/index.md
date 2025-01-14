# Обзор {{ ydb-full-name }}

*Yandex Database* ({{ ydb-short-name }}) — это горизонтально масштабируемая распределённая отказоустойчивая СУБД. {{ ydb-short-name }} спроектирована с учетом требований высокой производительности — например, обычный сервер может обрабатывать десятки тысяч запросов в секунду. В дизайн системы заложена работа с объемами данных в сотни петабайт.

{{ ydb-short-name }} обеспечивает:

* [строгую консистентность](https://en.wikipedia.org/wiki/Consistency_model#Strict_Consistency) с возможностью ослабления для увеличения производительности;
* подержку запросов [YQL](../../../yql/reference/overview.md) (диалект SQL для работы с большими данными);
* автоматическую репликацию данных;
* высокую доступность с автоматической обработкой отказов вычислительных узлов или зон доступности;
* автоматическое партицирование данных при увеличении их объема или увеличении нагрузки.

{{ ydb-short-name }} поддерживает реляционную [модель данных](../../../concepts/datamodel.md) и оперирует таблицами с предопределённой схемой. Для удобства организации таблиц поддерживается создание директорий по аналогии с файловой системой.

В {{ ydb-short-name }} поддерживаются высокопроизводительные распределенные [ACID](https://en.wikipedia.org/wiki/ACID_(computer_science))-транзакции, которые могут затрагивать несколько записей из разных таблиц. Обеспечивается самый строгий уровень изоляции транзакций — serializable. Также имеется возможность ослабления уровня изоляции для увеличения производительности.

В дизайн {{ ydb-short-name }} заложена поддержка разных сценариев нагрузки, таких как [OLTP](https://en.wikipedia.org/wiki/Online_transaction_processing) и [OLAP](https://en.wikipedia.org/wiki/Online_analytical_processing). В текущей реализации поддержка аналитических запросов ограничена. Поэтому можно говорить, что в данный момент YDB — это OLTP-база данных.
