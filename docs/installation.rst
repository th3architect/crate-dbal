============
Installation
============

Install the library by adding it to your ``composer.json`` or running::

    php composer.phar require crate/crate-dbal:~0.2.1

Then run ``composer install`` or ``composer update``.

Inside your PHP script you will need to require the autoload file::

    <?php
    require 'vendor/autoload.php';
    ...

For more information how to use Composer, please refer to the
`Composer documentation`_.


Configuration
=============

The Crate driver class is ``Crate\DBAL\Driver\PDOCrate\Driver``.

You can obtain a connection from the ``DriverManager`` using the following parameters::

    $params = array(
        'driverClass' => 'Crate\DBAL\Driver\PDOCrate\Driver',
        'host' => 'localhost',
        'port' => 4200
    );
    $connection = \Doctrine\DBAL\DriverManager::getConnection($params);
    $schemaManager = $connection->getSchemaManager();


.. _`Composer documentation`: https://getcomposer.org