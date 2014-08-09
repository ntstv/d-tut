Остальные языки программирования
===============

Считается что вы уже умеете программировать,
т.е пришли в D из другого языка.

C программисту
-----------------

В D вместо препроцессора используется более продвинутый механизм,
под названием мета программирование.
Почти весь C код компилируется в D, некоторые даже используют
D в качестве классного C компилятора.

  Я пишу свой C код на DMD.
  После отладки и настройки в D, я собираю финальную версию в C компиляторе.
  – `ed <http://forum.dlang.org/post/ibnfbsvxqzjxyfpnzseh@forum.dlang.org>`_


Стоит отметить, что D добавляет множество вещей, которы не определены (или не
возможны, трудно реализуемы) в C. Например, обертку для переполнения int'ов
(integer wraparound), что сейчас практически любая архитектура умеет.

Почему вы должны предпочти D? Мета программирование в D добавляет высоко-
уровневые абстракции, а значит уменьшает размер исходного кода. В D гораздо
меньше подводных камней, улучшенная и более безопасная типизация, мало
непредвиденного поведения и автоматическое управление памятью.

Java программисту
--------------------

В D есть классы, интерфейсы, модули, пакеты и встроенный сборщик мусора.
В D вы освоитесь очень быстро и почувствуете себя как дома. 
Вместо Java шаблонов есть D шаблоны.

 
Почему вы должны предпочти D? Мета программирование в D добавляет высоко-
уровневые абстракции, а значит уменьшает размер исходного кода. Для
чувствительных к ЦПУ или к памяти задач, когда они являются узким местом в
системе, D дает куда больше контроля и свободы действий для оптимизации.


C++ программисту
-------------------

Вы определенно почувствуете себя тут как дома.
Если вас впечатляют нововведения C++11,
вы будете в восторге от D.
В D даже есть то, чего нет в C++11.
Однако, придется привыкнуть к немного другому синтаксису.
D не обременен полной C подобной совместимостью.
Но можно линковать С и С++ библиотеки, после портирования
хэдеров.

Почему вы должны предпочти D? В D меньший наследственный мусор. Имеет меньше
подводных камней и безопаснее, благодаря предсказуемому поведению и
автоматическому управлению памятью.

C# программисту
------------------

Все очень похоже но немного по другому.
Почувствуете себя как дома, после того как привыкните что сходные вещи делаются
немного по другому.
Вместо расширения синтаксиса, типа LINQ,
D предоставляет множество сходных механизмов из стандартной библиотеки.
Вместо ``using``, в D есть защиты видимости.

Почему вы должны предпочти D? D не нужна виртуальная машина,
поэтому он годится для встроенных задач.

Node.js программисту
-----------------------

Syntactically, D looks familiar.
Note though, Javascripts ``function`` is ``delegate`` in D,
and Ds ``function`` is a lightweight variant without state.
D is statically typed,
but keeps the boilerplate low.
Here is `a Rosettacode example <http://rosettacode.org/wiki/Look-and-say_sequence#D>`_,
which shows a D program can be short and concise
or highly optimized.

Why would you prefer D?
If CPU or memory is a bottleneck,
D gives you much more control and room for optimization.
Look at `Vibe.d <http://vibed.org/>`_
"for easily building fast, scalable network applications".
This D framework is
"lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices."

For Clojure Programmers
-----------------------

D is no Lisp.
However, its meta programming is equally powerful and nearly as easy as Lisp macros.
D supports immutable data structures,
although the standard library is not that rich yet.
D is natively compiled and does not run on the JVM.

Why would you prefer D?
If CPU or memory is a bottleneck,
D gives you much more control and room for optimization.
The richer syntax of D might be more intuitive than Lisp expressions.

For Scala Programmers
---------------------

Like Scala,
D is multi-paradigm and combines object-oriented with functional concepts.
You can "construct elegant class hierarchies for maximum code reuse and extensibility, implement their behavior using higher-order functions" in D as well.

Why would you prefer D?
If CPU or memory is a bottleneck,
D gives you much more control and room for optimization.
Compiling D is much faster
and the speed of code-compile-test iterations is important for productivity.

For Go Programmers
------------------

Like Go,
D is natively compiled.
However, D has a much richer `feature set <http://dlang.org/comparison.html>`_.
This means,
where Go restricts you to carefully chosen selection of features,
D provides you the lower level building blocks.
The goroutine is called a
`fiber <http://dlang.org/phobos/core_thread.html#.Fiber>`_ in D
and `Vibe.d <http://vibed.org/>`_ is a nice framework around them.
Likewise,
a Go channel can be built using primitives from
`std.concurrency <http://dlang.org/phobos/std_concurrency.html>`_.
The structural typing of Go interfaces,
can be replicated with
`wrap and unwrap <http://dlang.org/phobos/std_typecons.html#.wrap>`_
from Ds standard library.

Why would you prefer D?
D supports generic programming,
which means less code and more type safety.
D provides a bigger toolbox to choose the right tool for the job.
Compiling D is as fast as compiling Go.

For Python-Ruby-Perl-Javascript-Lua Programmers
------------------------------------------

D is statically typed,
which probably takes some time to get used to.
However, D really tries to let you skip boilerplate.
Declare your variables with ``auto`` or ``const``.

.. code-block:: d

   auto x = 42;
   const y = "yes";

Also there is `Variant <http://dlang.org/phobos/std_variant.html>`_,
which can be used to put anything into a variable.

The D standard library strives to come with all batteries included.
Unfortunately, D is not as mature as Python.
While it is possible to be as terse in D,
often the libraries are missing for small scripting jobs.
You can use C/C++ libraries,
but that does not feel like batteries-included.
