BC XML Template Override Conditions
===================

This extension implements a solution to provide additional override.ini rules match condition support. Provides an extension based kernel class override for class, 'eZXMLOutputHandler'.

Version
=======

* The current version of BC XML Template Override Conditions is 0.1.0

* Last Major update: May 31, 2015


Copyright
=========

* BC XML Template Override Conditions is copyright 1999 - 2016 Brookins Consulting and 1999 - 2016 eZ Systems AS.

* See: [COPYRIGHT.md](COPYRIGHT.md) for more information on the terms of the copyright and license


License
=======

BC Document Reader is licensed under the GNU General Public License.

The complete license agreement is included in the [LICENSE](LICENSE) file.

BC Document Reader is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 2 of the License or at your
option a later version.

BC Document Reader is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

The GNU GPL gives you the right to use, modify and redistribute
BC Document Reader under certain conditions. The GNU GPL license
is distributed with the software, see the file doc/LICENSE.

It is also available at [http://www.gnu.org/licenses/gpl.txt](http://www.gnu.org/licenses/gpl.txt)

You should have received a copy of the GNU General Public License
along with BC Document Reader in doc/LICENSE.  If not, see [http://www.gnu.org/licenses/](http://www.gnu.org/licenses/).

Using BC Document Reader under the terms of the GNU GPL is free (as in freedom).

For more information or questions please contact: license@brookinsconsulting.com


Requirements
============

The following requirements exists for using BC XML Template Override Conditions extension:


### eZ Publish version

* Make sure you use eZ Publish version 5.x (required) or higher.

* Designed and tested with eZ Publish Community Project 2014.11


### PHP version

* Make sure you have PHP 5.x or higher.


Features
========

### Dependencies

* This solution depends on eZ Publish Legacy and kernel class overrides enabled in config.php


### Kernel class override

This solution overrides the following kernel class:

* PHP Class : `eZXMLOutputHandler` - Found by default at: `kernel/classes/datatypes/ezxmltext/ezxmloutputhandler.php`

This solution provides the following kernel class override:

* PHP Class : `eZXMLOutputHandler` - Found by at: `extension/bcxmltemplateoverrideconditions/classes/kerneloverride/kernel/classes/datatypes/ezxmltext/ezxmloutputhandler.php`


### Template override rule match conditions added

This solution provides the following ezxmltags template override rule match conditions you can use in your override.ini settings:

* Provided by default in eZ Publish:

    * attribute_identifier

* Added by bcxmltemplateoverrideconditions:

    *  object
    *  class
    *  class_identifier
    *  remote_id
    *  node
    *  node_remote_id
    *  depth
    *  url_alias
    *  parent_node
    *  parent_node_remote_id
    *  parent_object_remote_id
    *  parent_class
    *  parent_class_identifier

**Note**: Additional match conditions can be added by patching the kernel override class and documentation. We support with this solution nearly all possible match conditions (minus state and some other more obscure and rarely used conditions).


Installation
============

### Extension Installation via Composer

Run the following command from your project root to install the extension:

    bash$ composer require brookinsconsulting/bcxmltemplateoverrideconditions dev-master;


### Extension Activation

Kernel class override extensions are **not** activated via ini setttings. Normal site.ini extension activation settings are not required to use this extension and it's solution.


### Enable eZ Publish Kernel Overrides

Kernel class overrides are only able to be used if you add the following to your eZ Publish Legacy config.php configuration file.

    cp -va config.php-RECOMMENDED config.php;
    # Edit config.php to set 'EZP_AUTOLOAD_ALLOW_KERNEL_OVERRIDE' to true. It should look like this:
    define( 'EZP_AUTOLOAD_ALLOW_KERNEL_OVERRIDE', true );


### Regenerate kernel class override autoloads

Regenerate kernel class override autoloads (Required).

    php ./bin/php/ezpgenerateautoloads.php --kernel-override;


### Clear the caches

Clear eZ Publish Platform / eZ platfrom caches (Required).

    php ./bin/php/ezcache.php --clear-all;


Usage
=====

The solution is configured to work virtually by default once properly installed.

You can use the additional override.ini rules match conditions within your settings to use this solution's features


Troubleshooting
===============

### Read the FAQ

Some problems are more common than others. The most common ones are listed in the the [doc/FAQ.md](doc/FAQ.md)


### Support

If you have find any problems not handled by this document or the FAQ you can contact Brookins Consulting through the support system: [http://brookinsconsulting.com/contact](http://brookinsconsulting.com/contact)

