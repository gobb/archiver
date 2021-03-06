Lootils Archiver
==============

An abstraction library to interface with file archives.

[![Build Status](https://secure.travis-ci.org/lootils/archiver.png?branch=master)](http://travis-ci.org/lootils/archiver)


Installation
-----------

Use [Composer](http://getcomposer.org) to retrieve Archiver's dependencies:

    curl -s http://getcomposer.org/installer | php
    php composer.phar install


Usage
-----

Create a zip file:

    $zip = \Lootils\Archiver\ZipArchive('myarchive.zip');
    $zip->add('myfile.png');


Extract a .tar archive:

    $tar = \Lootils\Archiver\TarArchive('myarchive.tar');
    $tar->extract('destination');


List the contents of an archive:

    $tar = \Lootils\Archiver\TarArchive('myarchive.tar');
    $files = $tar->contents();
    foreach ($files as $filename => $data) {
       echo $filename . ' ';
    }


Development
----------

To install development tools, run the following:

    curl -s http://getcomposer.org/installer | php
    php composer.phar install --dev


Run tests:

    php vendor/bin/phpunit -c tests


Fix code standards:

    php vendor/bin/php-cs-fixer fix .


License
------

Lootils Archiver is licensed under the New BSD License - see the LICENSE file
for details.
