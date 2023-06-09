Introduction
============

DoctrineModule provides a bridge between `Laminas <https://getlaminas.org/>`__ and Doctrine. It
gives you access to features that can be used across
`Doctrine ORM <https://www.doctrine-project.org/projects/doctrine-orm/en/current/index.html>`__ as well as
`Doctrine MongoDB ODM <https://www.doctrine-project.org/projects/doctrine-mongodb-odm/en/current/index.html>`__.
It provides an abstraction layer on top of
`Doctrine\Common <https://www.doctrine-project.org/projects/doctrine-common/en/current/index.html>`__
which allows the end user to build functionality being completely unaware if he’s currently working
with Doctrine ORM or Doctrine MongoDB ODM.

To use Doctrine ORM or ODM, you will need
`DoctrineORMModule <https://www.doctrine-project.org/projects/doctrine-orm-module/en/current/index.html>`__ or
`DoctrineMongoODMModule <https://www.doctrine-project.org/projects/doctrine-mongo-odm-module/en/current/index.html>`__
respectively.

Installation
------------

Run the following to install this library using `Composer <https://getcomposer.org/>`__:

.. code:: bash

   $ composer require doctrine/doctrine-module

Note on PHP 8.0 or later
^^^^^^^^^^^^^^^^^^^^^^^^

This module provides an integration with
`laminas-cache <https://docs.laminas.dev/laminas-cache/>`__, which currently comes
with some storage adapters which are not compatible with PHP 8.0 or later. To prevent
installation of these unused cache adapters, you will need to add the following to
your ``composer.json`` file:

.. code:: json

    "require": {
         "doctrine/doctrine-module": "^4.4.0"
    },
    "replace": {
        "laminas/laminas-cache-storage-adapter-apc": "*",
        "laminas/laminas-cache-storage-adapter-dba": "*",
        "laminas/laminas-cache-storage-adapter-memcache": "*",
        "laminas/laminas-cache-storage-adapter-memcached": "*",
        "laminas/laminas-cache-storage-adapter-mongodb": "*",
        "laminas/laminas-cache-storage-adapter-wincache": "*",
        "laminas/laminas-cache-storage-adapter-xcache": "*",
        "laminas/laminas-cache-storage-adapter-zend-server": "*"
    }

Consult the `laminas-cache documentation <https://docs.laminas.dev/laminas-cache/installation/#avoid-unused-cache-adapters-are-being-installed>`__
for further information on this issue.

Next Steps
----------

You can find more details about the features offered by DoctrineModule:

-  :doc:`Authentication documentation <authentication>`:
   this explains how you can use the DoctrineModule authentication
   adapter and authentication storage adapter to provide a simple way to
   authenticate users using Doctrine.
-  :doc:`Caching documentation <caching>`:
   DoctrineModule provides simple classes to allow easier caching using
   Doctrine.
-  :doc:`CLI documentation <cli>`:
   learn how to use the Doctrine 2 command line tool, and how to add
   your own command.
-  :doc:`Form elements <form-element>`:
   if you are using Laminas Forms, this module provides select, radio and
   checkbox elements for selecting objects from relationships.
-  `Hydrator
   documentation <https://www.doctrine-project.org/projects/doctrine-laminas-hydrator.html>`__:
   if you are using Laminas Forms,
   ``doctrine-laminas-hydrator`` provides a powerful hydrator that allows
   you to easily deal with OneToOne, OneToMany and ManyToOne
   relationships when using forms.
-  :doc:`Paginator documentation <paginator>`:
   discover how to use the DoctrineModule Paginator adapter.
-  :doc:`Validator documentation <validator>`:
   this chapter explains how to use ObjectExists and NoObjectExists
   validator, that allow you to easily validate if a given entity exists
   or not.
