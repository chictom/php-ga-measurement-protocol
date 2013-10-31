Google Analytics Measurement Protocol PHP Client
===========================================================================================

[![Build Status](https://travis-ci.org/krizon/php-ga-measurement-protocol.png?branch=master)](https://travis-ci.org/krizon/php-ga-measurement-protocol)
[![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/krizon/php-ga-measurement-protocol/badges/quality-score.png?s=690ba3465d629f9876678af9ae4a41a346c994ab)](https://scrutinizer-ci.com/g/krizon/php-ga-measurement-protocol/)

This library is currently in development but will be tagged 1.0 by the end of november 2013 when all
features are implemented.

See https://developers.google.com/analytics/devguides/collection/protocol/v1/devguide

Features
-------------------------------------------------------------------------------------------
- Page tracking
- Event tracking
- Ecommerce tracking (todo)
- Social interactions tracking (todo)
- Exception tracking (todo)
- User timing tracking (todo)
- App tracking (todo)
- Non-blocking requests (todo)

Testing
-------------------------------------------------------------------------------------------
Before you can run the tests make sure you installed the dependencies using composer:

```$ composer install```

PHPUnit itself is included in the dependencies so now you can call:

```$ vendor/bin/phpunit```

We have two types of test:

* Tests with mocked 200 OK response, @group __nogroup__. This type of tests are used tor testing required fields,
asserting classtypes etc.;
* Tests that do real calls to the Google API, @group internet. The Google API itself always returns a 200 OK so to
be sure the requests are transferred and handled correctly you can run the tests of group 'internet'. Before running
this group make sure you've configured the correct tracking id in the phpunit.xml configuration by set the env variable
```tracking_id```. This group is excluded by default but you can run this tests by calling:
```$ vendor/bin/phpunit --group internet```
