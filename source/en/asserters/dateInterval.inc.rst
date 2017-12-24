.. _date-interval:

dateInterval
************

It's the assertion dedicated to `DateInterval <http://php.net/dateinterval>`_ object.

If you try to test a value that is not a ``DateInterval`` (or a child class) with this assertion it will fail.

.. _date-interval-is-clone-of:

isCloneOf
=========

.. seealso::
   ``isCloneOf`` is a method inherited from asserter ``object``.
   For more information, refer to the documentation of :ref:`object::isCloneOf <object-is-clone-of>`


.. _date-interval-is-equal-to:

isEqualTo
=========

``isEqualTo`` checks that the duration of object ``DateInterval`` is equals to to the duration of another ``DateInterval`` object.

.. code-block:: php

   <?php
   $di = new DateInterval('P1D');

   $this
       ->dateInterval($di)
           ->isEqualTo(                // passes
               new DateInterval('P1D')
           )
           ->isEqualTo(                // fails
               new DateInterval('P2D')
           )
   ;

.. _date-interval-is-greater-than:

isGreaterThan
=============

``isGreaterThan`` checks that the duration of the object  ``DateInterval`` is higher to the duration of the given ``DateInterval`` object.

.. code-block:: php

   <?php
   $di = new DateInterval('P2D');

   $this
       ->dateInterval($di)
           ->isGreaterThan(            // passes
               new DateInterval('P1D')
           )
           ->isGreaterThan(            // fails
               new DateInterval('P2D')
           )
   ;

.. _date-interval-is-greater-than-or-equal-to:

isGreaterThanOrEqualTo
======================

``isGreaterThanOrEqualTo`` checks that the duration of the object ``DateInterval`` is higher or equals to the duration of another object ``DateInterval``.

.. code-block:: php

   <?php
   $di = new DateInterval('P2D');

   $this
       ->dateInterval($di)
           ->isGreaterThanOrEqualTo(   // passes
               new DateInterval('P1D')
           )
           ->isGreaterThanOrEqualTo(   // passes
               new DateInterval('P2D')
           )
           ->isGreaterThanOrEqualTo(   // fails
               new DateInterval('P3D')
           )
   ;

.. _date-interval-is-identical-to:

isIdenticalTo
=============

.. seealso::
   ``isIdenticalTo`` is an inherited method from ``object`` asserter.
   For more information, refer to the documentation of :ref:`object::isIdenticalTo <object-is-identical-to>`


.. _date-interval-is-instance-of:

isInstanceOf
============

.. seealso::
   ``isInstanceOf`` is a method inherited from asserter ``object``.
   For more information, refer to the documentation of :ref:`object::isInstanceOf <object-is-instance-of>`


.. _date-interval-is-less-than:

isLessThan
==========

``isLessThan`` checks that the duration of the object  ``DateInterval`` is lower than the duration of the given ``DateInterval`` object.

.. code-block:: php

   <?php
   $di = new DateInterval('P1D');

   $this
       ->dateInterval($di)
           ->isLessThan(               // passes
               new DateInterval('P2D')
           )
           ->isLessThan(               // fails
               new DateInterval('P1D')
           )
   ;

.. _date-interval-is-less-than-or-equal-to:

isLessThanOrEqualTo
===================

``isLessThanOrEqualTo`` checks that the duration of the object ``DateInterval`` is lower or equals to the duration of another object ``DateInterval``.

.. code-block:: php

   <?php
   $di = new DateInterval('P2D');

   $this
       ->dateInterval($di)
           ->isLessThanOrEqualTo(      // passes
               new DateInterval('P3D')
           )
           ->isLessThanOrEqualTo(      // passes
               new DateInterval('P2D')
           )
           ->isLessThanOrEqualTo(      // fails
               new DateInterval('P1D')
           )
   ;

.. _date-interval-is-not-equal-to:

isNotEqualTo
============

.. seealso::
   ``isNotEqualTo`` is a method inherited from ``object`` asserter.
   For more information, refer to the documentation of :ref:`object::isNotEqualTo <object-is-not-equal-to>`


.. _date-interval-is-not-identical-to:

isNotIdenticalTo
================

.. seealso::
   ``isNotIdenticalTo`` is an inherited method from ``object`` asserter.
   For more information, refer to the documentation of :ref:`object::isNotIdenticalTo <object-is-not-identical-to>`


.. _date-interval-is-zero:

isZero
======

``isZero`` check the duration of ``DateInterval`` is equal to 0.

.. code-block:: php

   <?php
   $di1 = new DateInterval('P0D');
   $di2 = new DateInterval('P1D');

   $this
       ->dateInterval($di1)
           ->isZero()      // passes
       ->dateInterval($di2)
           ->isZero()      // fails
   ;
