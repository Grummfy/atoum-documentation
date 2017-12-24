.. _size-of:

sizeOf
******

C'est l'assertion dédiée aux tests sur la taille des tableaux et des objets implémentant l'interface ``Countable``.

.. code-block:: php

   <?php
   $array           = array(1, 2, 3);
   $countableObject = new GlobIterator('*');

   $this
       ->sizeOf($array)
           ->isEqualTo(3)

       ->sizeOf($countableObject)
           ->isGreaterThan(0)
   ;

.. _size-of-is-equal-to:

isEqualTo
=========

.. seealso::
   ``isEqualTo`` est une méthode héritée de l'asserter ``variable``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`variable::isEqualTo <variable-is-equal-to>`


.. _size-of-is-greater-than:

isGreaterThan
=============

.. seealso::
   ``isGreaterThan`` est une méthode héritée de l'asserter ``integer``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`integer::isGreaterThan <integer-is-greater-than>`


.. _size-of-is-greater-than-or-equal-to:

isGreaterThanOrEqualTo
======================

.. seealso::
   ``isGreaterThanOrEqualTo`` est une méthode héritée de l'asserter ``integer``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`integer::isGreaterThanOrEqualTo <integer-is-greater-than-or-equal-to>`


.. _size-of-is-identical-to:

isIdenticalTo
=============

.. seealso::
   ``isIdenticalTo`` est une méthode héritée de l'asserter ``variable``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`variable::isIdenticalTo <variable-is-identical-to>`


.. _size-of-is-less-than:

isLessThan
==========

.. seealso::
   ``isLessThan`` est une méthode héritée de l'asserter ``integer``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`integer::isLessThan <integer-is-less-than>`


.. _size-of-is-less-than-or-equal-to:

isLessThanOrEqualTo
===================

.. seealso::
   ``isLessThanOrEqualTo`` est une méthode héritée de l'asserter ``integer``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`integer::isLessThanOrEqualTo <integer-is-less-than-or-equal-to>`


.. _size-of-is-not-equal-to:

isNotEqualTo
============

.. seealso::
   ``isNotEqualTo`` est une méthode héritée de l'asserter ``variable``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`variable::isNotEqualTo <variable-is-not-equal-to>`


.. _size-of-is-not-identical-to:

isNotIdenticalTo
================

.. seealso::
   ``isNotIdenticalTo`` est une méthode héritée de l'asserter ``variable``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`variable::isNotIdenticalTo <variable-is-not-identical-to>`


.. _size-of-is-zero:

isZero
======

.. seealso::
   ``isZero`` est une méthode héritée de l'asserter ``integer``.
   Pour plus d'informations, reportez-vous à la documentation de :ref:`integer::isZero <integer-is-zero>`
