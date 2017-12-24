.. _utf8-string:

utf8String
**********

It's the asserter dedicated to UTF-8 strings.

.. note::
   ``utf8Strings`` use the functions ``mb_*`` to manage multi-byte strings. Refer to the PHP manual for more information about `mbstring <http://php.net/mbstring>`_ extension.


.. _utf8-string-contains:

contains
========

.. seealso::
   ``contains`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::contains <string-contains>`


.. _utf8-string-has-length:

hasLength
=========

.. seealso::
   ``hasLength`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::hasLength <string-has-length>`


.. _utf8-string-has-length-greater-than:

hasLengthGreaterThan
====================

.. seealso::
   ``hasLengthGreaterThan`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::hasLengthGreaterThan <string-has-length-greater-than>`


.. _utf8-string-has-length-less-than:

hasLengthLessThan
=================

.. seealso::
   ``hasLengthLessThan`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::hasLengthLessThan <string-has-length-less-than>`


.. _utf8-string-is-empty:

isEmpty
=======

.. seealso::
   ``isEmpty`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::isEmpty <string-is-empty>`


.. _utf8-string-is-equal-to:

isEqualTo
=========

.. seealso::
   ``isEqualTo`` is a method inherited from the ``variable`` asserter.
   For more information, refer to the documentation of :ref:`variable::isEqualTo <variable-is-equal-to>`


.. _utf8-string-is-equal-to-contents-of-file:

isEqualToContentsOfFile
=======================

.. seealso::
   ``isEqualToContentsOfFile`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::isEqualToContentsOfFile <string-is-equal-to-contents-of-file>`


.. _utf8-string-is-identical-to:

isIdenticalTo
=============

.. seealso::
   ``isIdenticalTo`` is a method inherited from the ``variable`` asserter.
   For more information, refer to the documentation of :ref:`variable::isIdenticalTo <variable-is-identical-to>`


.. _utf8-string-is-not-empty:

isNotEmpty
==========

.. seealso::
   ``isNotEmpty`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::isNotEmpty <string-is-not-empty>`


.. _utf8-string-is-not-equal-to:

isNotEqualTo
============

.. seealso::
   ``isNotEqualTo`` is a method inherited from the ``variable`` asserter.
   For more information, refer to the documentation of :ref:`variable::isNotEqualTo <variable-is-not-equal-to>`


.. _utf8-string-is-not-identical-to:

isNotIdenticalTo
================

.. seealso::
   ``isNotIdenticalTo`` is a method inherited from the ``variable`` asserter.
   For more information, refer to the documentation of :ref:`variable::isNotIdenticalTo <variable-is-not-identical-to>`


.. _utf8-string-matches:

matches
=======

.. hint::
   ``matches`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::match <string-matches>`


.. note::
   Remember to add ``u`` in your regular expression, in the option part.
   For more precision, read the PHP's documentation about `the options for search in regular expression  <http://php.net/reference.pcre.pattern.modifiers>`_.


.. code-block:: php

   <?php
   $vdm = "Today at 57 years, my father got a tatoo of a Unicorn on his shoulder. FML";

   $this
       ->utf8String($vdm)
           ->matches("#^Today.*VDM$#u")
   ;

.. _utf8-string-not-contains:

notContains
===========

.. seealso::
   ``notContains`` is a method inherited from the ``string`` asserter.
   For more information, refer to the documentation of :ref:`string::notContains <string-not-contains>`
