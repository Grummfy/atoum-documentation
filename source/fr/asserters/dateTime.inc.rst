.. _date-time:

dateTime
********

C'est l'assertion dédiée à l'objet `DateTime <http://php.net/datetime>`_.

Si vous essayez de tester une variable qui n'est pas un objet ``DateTime`` (ou une classe qui l'étend) avec cette assertion, cela échouera.

.. _date-time-has-date:

hasDate
=======

``hasDate`` vérifie la partie date de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('1981-02-13');

   $this
       ->dateTime($dt)
           ->hasDate('1981', '02', '13')   // passe
           ->hasDate('1981', '2',  '13')   // passe
           ->hasDate(1981,   2,    13)     // passe
   ;

.. _date-time-has-date-and-time:

hasDateAndTime
==============

``hasDateAndTime`` vérifie la partie date et heure de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('1981-02-13 01:02:03');

   $this
       ->dateTime($dt)
           // passe
           ->hasDateAndTime('1981', '02', '13', '01', '02', '03')
           // passe
           ->hasDateAndTime('1981', '2',  '13', '1',  '2',  '3')
           // passe
           ->hasDateAndTime(1981,   2,    13,   1,    2,    3)
   ;

.. _date-time-has-day:

hasDay
======

``hasDay`` vérifie le jour de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('1981-02-13');

   $this
       ->dateTime($dt)
           ->hasDay(13)        // passe
   ;

.. _date-time-has-hours:

hasHours
========

``hasHours`` vérifie l'heure de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('01:02:03');

   $this
       ->dateTime($dt)
           ->hasHours('01')    // passe
           ->hasHours('1')     // passe
           ->hasHours(1)       // passe
   ;

.. _date-time-has-minutes:

hasMinutes
==========

``hasMinutes`` vérifie les minutes de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('01:02:03');

   $this
       ->dateTime($dt)
           ->hasMinutes('02')  // passe
           ->hasMinutes('2')   // passe
           ->hasMinutes(2)     // passe
   ;

.. _date-time-has-month:

hasMonth
========

``hasMonth`` vérifie le mois de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('1981-02-13');

   $this
       ->dateTime($dt)
           ->hasMonth(2)       // passe
   ;

.. _date-time-has-seconds:

hasSeconds
==========

``hasSeconds`` vérifie les secondes de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('01:02:03');

   $this
       ->dateTime($dt)
           ->hasSeconds('03')    // passe
           ->hasSeconds('3')     // passe
           ->hasSeconds(3)       // passe
   ;

.. _date-time-has-time:

hasTime
=======

``hasTime`` vérifie le temps de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('01:02:03');

   $this
       ->dateTime($dt)
           ->hasTime('01', '02', '03')     // passe
           ->hasTime('1',  '2',  '3')      // passe
           ->hasTime(1,    2,    3)        // passe
   ;

.. _date-time-has-timezone:

hasTimezone
===========

``hasTimezone`` vérifie le fuseau horaire de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime();

   $this
       ->dateTime($dt)
           ->hasTimezone('Europe/Paris')
   ;

.. _date-time-has-year:

hasYear
=======

``hasYear`` vérifie l'année de l'objet ``DateTime``.

.. code-block:: php

   <?php
   $dt = new DateTime('1981-02-13');

   $this
       ->dateTime($dt)
           ->hasYear(1981)     // passe
   ;

.. _date-time-is-clone-of:

isCloneOf
=========

.. seealso::
   ``isCloneOf`` est une méthode héritée de l'asserter ``object``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`object::isCloneOf <object-is-clone-of>`


.. _date-time-is-equal-to:

isEqualTo
=========

.. seealso::
   ``isEqualTo`` est une méthode héritée de l'asserter ``object``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`object::isEqualTo <object-is-equal-to>`


.. _dat-time-is-identical-to:

isIdenticalTo
=============

.. seealso::
   ``isIdenticalTo`` est une méthode héritée de l'asserter ``object``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`object::isIdenticalTo <object-is-identical-to>`

.. _date-time-is-immutable:

isImmutable
===========

``isImmutable`` vérifie que qu'un objet ``DateTime`` est immuable.

.. code-block:: php

   <?php
   $dt = new DateTime('1981-02-13');

   $this
       ->dateTime($dt)
           ->isImmutable(1981)     // rate
   ;

   $dt = new DateTimeImmutable('1981-02-13');

   $this
       ->dateTime($dt)
           ->isImmutable(1981)     // réussit
   ;

.. _date-time-is-instance-of:

isInstanceOf
============

.. seealso::
   ``isInstanceOf`` est une méthode héritée de l'asserter ``object``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`object::isInstanceOf <object-is-instance-of>`


.. _date-time-is-not-equal-to:

isNotEqualTo
============

.. seealso::
   ``isNotEqualTo`` est une méthode héritée de l'asserter ``object``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`object::isNotEqualTo <object-is-not-equal-to>`


.. _date-time-is-not-identical-to:

isNotIdenticalTo
================

.. seealso::
   ``isNotIdenticalTo`` est une méthode héritée de l'asserter ``object``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`object::isNotIdenticalTo <object-is-not-identical-to>`
