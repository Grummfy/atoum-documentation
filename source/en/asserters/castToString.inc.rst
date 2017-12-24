.. _cast-to-string:

castToString
************

It's the assertion dedicated to tests on the cast of objects to strings.

.. code-block:: php

   <?php
   class AtoumVersion {
       private $version = '1.0';

       public function __toString() {
           return 'atoum v' . $this->version;
       }
   }

   $this
       ->castToString(new AtoumVersion())
           ->isEqualTo('atoum v1.0')
   ;

.. _cast-to-string-contains:

contains
========

.. seealso::
   ``contains`` is a method herited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::contains <string-contains>`


.. _cast-to-string-not-contains:

notContains
===========

.. seealso::
   ``notContains`` is a method herited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::notContains <string-not-contains>`


.. _cast-to-string-has-length:

hasLength
=========

.. seealso::
   ``hasLength`` is a method herited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::hasLength <string-has-length>`


.. _cast-to-string-has-length-greater-than:

hasLengthGreaterThan
====================

.. seealso::
   ``hasLengthGreaterThan`` is a method inherited from ``string`` asserter.
   For more information, refer to the documentation  for :ref:`string::hasLengthGreaterThan <string-has-length-greater-than>`


.. _cast-to-string-has-length-less-than:

hasLengthLessThan
=================

.. seealso::
   ``hasLengthLessThan`` is a method inherited from ``string`` asserter.
   For more information, refer to the documentation  for :ref:`string::hasLengthLessThan <string-has-length-less-than>`


.. _cast-to-string-is-empty:

isEmpty
=======

.. seealso::
   ``isEmpty`` is a method inherited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::isEmpty <string-is-empty>`


.. _cast-to-string-is-equal-to:

isEqualTo
=========

.. seealso::
   ``isEqualTo`` is a method inherited from ``variable`` asserter.
   For more information, refer to the documentation of  :ref:`variable::isEqualTo <variable-is-equal-to>`


.. _cast-to-string-is-equal-to-contents-of-file:

isEqualToContentsOfFile
=======================

.. seealso::
   ``isEqualToContentsOfFile`` is a method inherited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::isEqualToContentsOfFile <string-is-equal-to-contents-of-file>`


.. _cast-to-string-is-identical-to:

isIdenticalTo
=============

.. seealso::
   ``isIdenticalTo`` is a method inherited from ``variable`` asserter.
   For more information, refer to the documentation of  :ref:`variable::isIdenticalTo <variable-is-identical-to>`


.. _cast-to-string-is-not-empty:

isNotEmpty
==========

.. seealso::
   ``isNotEmpty`` is a method inherited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::isNotEmpty <string-is-not-empty>`


.. _cast-to-string-is-not-equal-to:

isNotEqualTo
============

.. seealso::
   ``isNotEqualTo`` is a method inherited from ``variable`` asserter.
   For more information, refer to the documentation of  :ref:`variable::isNotEqualTo <variable-is-not-equal-to>`


.. _cast-to-string-is-not-identical-to:

isNotIdenticalTo
================

.. seealso::
   ``isNotIdenticalTo`` is a method inherited from ``variable`` asserter.
   For more information, refer to the documentation of  :ref:`variable::isNotIdenticalTo <variable-is-not-identical-to>`


.. _cast-to-string-matches:

matches
=======

.. seealso::
   ``matches`` is a method inherited from ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::match <string-matches>`
