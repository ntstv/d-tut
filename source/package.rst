Пакеты
======

Видимо dub станет основным кандитатом на каноничный менеджер пакетов для D.
Ему необходим простой JSON документ заданной структуры ``package.json`` для описания проекта.

* исходный код должен лежать в подпапке ``source`` или ``src``
* main должен быть в ``app.d`` или ``<package name>.d``
* строковый импорт в ``views``.

Главное хранилище кода хостится на `code.dlang.org <http://code.dlang.org/>`_.
Это практически официальный аналог к PAN, PyPI, RubyGems, NPM, и т. д.
Загрузить dub вы можете `тут <http://code.dlang.org/download>`_.

Dub пример
----------

В качестве примера рассмотрим `DDox <https://github.com/rejectedsoftware/ddox>`_,
отличный генератор документации,
который немного сложнее чем встроенный.
Если dub установлен, то вот так вы можете получить ddox.

.. code-block:: sh

   git clone https://github.com/rejectedsoftware/ddox.git
   cd ddox
   dub build

После загрузки кода из гитхаба,
комманда ``dub build``
проверит и установит все dub зависимости (vibe.d, libevent, libev, openssl)
и соберет ddox.
Однако, под Linux lib* dub пакеты содержат только байндинги,
недостающие библиотеки придется установить вручную, чтобы не получить
ошибок линковки.

.. seealso::

   `Primary D package index <http://code.dlang.org>`_
