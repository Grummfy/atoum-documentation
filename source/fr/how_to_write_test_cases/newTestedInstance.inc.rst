
.. _newTestedInstance:

newTestedInstance & testedInstance
**********************************

Lorsque l'on effectue des tests, il faut bien souvent créer une nouvelle instance de la classe et passer celle-ci dans divers paramètres. Une aide à l'écriture est disponible pour ce cas précis, il s'agit de ``newTestedInstance`` et de ``testedInstance``

Voici un exemple :

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

Ceci peut être simplifié avec la nouvelle syntaxe :

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


Comme on le voit, c'est légèrement plus simple, mais surtout cela présente deux avantages :

* On ne manipule pas le nom de la classe testée
* On ne manipule pas l'instance ainsi créée

Par ailleurs, on peut facilement valider que l'on a bien l'instance testée avec :ref:`isTestedInstance<object-is-tested-instance>`, comme expliqué dans l'exemple précédent.

Pour passer des arguments au constructeur, il suffit de le faire au travers de ``newTestedInstance`` :

.. code-block:: php

   $this->newTestedInstance($argument1, $argument2);


Si vous voulez tester une méthode statique de votre classe, vous pouvez récupérer la classe testée avec cette syntaxe :

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

Accès aux constantes de la classe testée
========================================

Si vous avez besoin d’accéder aux constantes de la classe testée, vous pouvez y accéder de deux façons :

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

.. warning::
	Vous avez besoin d'initialiser l'instance avec ``newTestedInstance``, pour avoir accès aux constantes.

.. _testedClass:

testedClass
***********

Comme ``testedInstance``, vous pouvez utiliser ``testedClass`` pour écrire des tests plus compréhensible. ``testedClass`` permet d'écrire des assertions dynamiques sur les classes testées :

.. code-block:: php

	<?php
	$this
		->testedClass
            ->hasConstant('FOO')
			->isFinal()
	;

Vous pouvez aller plus loin avec :ref:`les assertions de classe<class-anchor>`.
