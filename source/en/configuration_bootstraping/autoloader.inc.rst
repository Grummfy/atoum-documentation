
.. _autoloader_file:

Autoloader file
***************

The autoloader file is the way you will define how the class to test will be found by atoum.

The default name of the file is ``.autoloader.atoum.php``, atoum will load it automatically if this file is located in the current directory. You can define it through the cli with ``--autoloader-file`` or ``-af``
(:ref:`see the cli options<cli-options-autoloader_file>`). The purpose of the autoloading file is to find the way to load the classes mandatory to run the tests. You can find more information about
`autoloading <http://php.net/manual/fr/function.autoload.php>`_ in the php manual.

If the autoloader file doesn't exist, atoum will try to load ``vendor/autoload.php`` from composer. So most of the time, you will have nothing to do ;).
