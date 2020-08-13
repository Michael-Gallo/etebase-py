# Changelog

## Version 0.12.1
* Change how we import scrypt from hashlib to be more pythonic

## Version 0.12.0
* Update cryptography dep

## Version 0.11.1
* Use the hashlib scrypt implementation if available, otherwise fallback to scrypt or pyscrypt

## Version 0.11.0
* Make sync faster by only fetching entries when journals have changed.
* Change the scrypt dep in setup.py to scrypt (from pyscrypt, which is still supported as a fallback).
* Set the user agent when making requests.

## Version 0.10.0
* Change database model to WAL which should improve concurrency

## Version 0.9.3
* Provide more explicit copyright and licensing information.

## Version 0.9.2
* Remove dev dep (coverage) from setup.py

## Version 0.9.1
* Gracefully handle entries without a UID.

## Version 0.9.0
* Fix reinit of the EteSync object (fixes tests)
* Bump minor version as should have been done in the previous release.

## Version 0.8.4
* Allow users of this library to add tables to the cache database.
* Make the sqlite database more strict (enforce foreign key relations).

## Version 0.8.3
* Fix typo with pytz dependency

## Version 0.8.2
* Add missing pytz dependency
* Upgrade urllib3 and requests

## Version 0.8.1
* Fix pushing entries to shared journals.

## Version 0.8.0
* Add support for read only journals
* Fix issue with having the same journals in the db for different users.
* Journal list fetching: fix stale cache issue.

## Version 0.7.0
* Fix user info to use the correct asymmetric key format
* Sync user info on every protocol sync - needed for encryption password changes.

## Version 0.6.3
* Sync: automatically create user info if doesn't exist

## Version 0.6.2
* Add shell scripts for executing tests

## Version 0.6.1
* Fix journal integrity issue when syncing more than one collection item.

## Version 0.6.0
* Add tasks support

## Version 0.5.6
* Fix broken calling to scrypt
* Fix sync (was broken in some cases) and tests

## Version 0.5.5
* Automatically detect if scrypt is available. If so use it, otherwise revert to pyscript. Setup.py dep remains on pyscypt.
  * This is to help distros that don't package pyscrypt
* Update peewee to support version 3 and up

## Version 0.5.4
* Fix peewee dep to be < 3.0.0

## Version 0.5.3
* Change back to pyscript, because scrypt has proven very problematic
* Update all the deps

## Version 0.5.2
* Don't install tests as a package

## Version 0.5.1
* Change from pyscrypt to scrypt (much faster and widely adopted)

## Version 0.5.0
* Add functions to check if the journal list or journals are dirty.
* Add a nicer way to access the journal's info.
* Fix an issue with caching user info
* Improve tests
