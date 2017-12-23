
.. _newTestedInstance:

newTestedInstance & testedInstance
**********************************

When performing tests, we must often create a new instance of the class and pass it through parameters. Writing helper are available for this specific case, it's ``newTestedInstance`` and ``testedInstance``

Here's an example :

.. code-block:: php

   namespace jubianchi\atoum\preview\tests\units;
   
   use atoum;
   use jubianchi\atoum\preview\foo as testedClass;
   
   class foo extends atoum
   {
       public function testBar()
       {
           $this
               ->if($foo = new testedClass())
               ->then
                   ->object($foo->bar())->isIdenticalTo($foo)
           ;
       }
   }

This can be simplified with a new syntax:

.. code-block:: php

   namespace jubianchi\atoum\preview\tests\units;
   
   use atoum;
   
   class foo extends atoum
   {
       public function testBar()
       {
           $this
               ->if($this->newTestedInstance)
               ->then
                   ->object($this->testedInstance->bar())
                       ->isTestedInstance()
           ;
       }
   }


As seen, it's slightly simpler but especially this has two advantages:

* We do not manipulate the name of the tested class
* We do not manipulate the tested instance

Furthermore, we can easily validate that the instance is available with :ref:`isTestedInstance<object-is-tested-instance>`, as explained in the previous example.

To pass some arguments to the constructor, it's easy through ``newTestedInstance``:

.. code-block:: php

   $this->newTestedInstance($argument1, $argument2);


If you want to test a static method of your class, you can retrieve the tested class with this syntax:

.. code-block:: php

   namespace jubianchi\atoum\preview\tests\units;
   
   use atoum;
   
   class foo extends atoum
   {
       public function testBar()
       {
         $this
           ->if($class = $this->testedClass->getClass())
           ->then
             ->object($class::bar())
          ;
       }
    }


.. _testedInstance-class:

Accessing constant of the tested class
======================================

If you require to access to the constant of your tested class, you can access it in two ways:

.. code-block:: php

	<?php

	namespace
	{
	    class Foo
	    {
	        const A = 'a';
	    }
	}

	namespace tests\units
	{
	    class Foo extends \atoum\test
	    {
	        public function testFoo()
	        {
	            $this
	                ->given($this->newTestedInstance())
	                ->then
	                    ->string($this->getTestedClassName()::A)->isEqualTo('a')
	                    ->string($this->testedInstance::A)->isEqualTo('a')
	            ;
	        }
	    }
	}

.. remarks::
	You firstly need to initiate the instance with the ``newTestedInstance``, to have access to constant.

.. _testedClass:

testedClass
***********

Like ``testedInstance``, you can use ``testedClass`` to write more comprehensible test. ``testedClass`` allows you to dynamically assert on the class being tested:

.. code-block:: php

	<?php
	$this
		->testedClass
            ->hasConstant('FOO')
			->isFinal()
	;

You can go further with the :ref:`class asseters<class-anchor>`.
