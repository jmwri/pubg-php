# PUBG

[![Build Status](https://travis-ci.org/jmwri/pubg-php.svg?branch=master)](https://travis-ci.org/jmwri/pubg-php)
[![Total Downloads](https://poser.pugx.org/jmwri/pubg-php/d/total.svg)](https://packagist.org/packages/jmwri/pubg-php)
[![Latest Stable Version](https://poser.pugx.org/jmwri/pubg-php/v/stable.svg)](https://packagist.org/packages/jmwri/pubg-php)
[![Latest Unstable Version](https://poser.pugx.org/jmwri/pubg-php/v/unstable.svg)](https://packagist.org/packages/jmwri/pubg-php)
[![License](https://poser.pugx.org/jmwri/pubg-php/license.svg)](https://packagist.org/packages/jmwri/pubg-php)
[![Code Climate](https://codeclimate.com/github/jmwri/pubg-php/badges/gpa.svg)](https://codeclimate.com/github/jmwri/pubg-php)
[![Test Coverage](https://codeclimate.com/github/jmwri/pubg-php/badges/coverage.svg)](https://codeclimate.com/github/jmwri/pubg-php/coverage)
[![Issue Count](https://codeclimate.com/github/jmwri/pubg-php/badges/issue_count.svg)](https://codeclimate.com/github/jmwri/pubg-php)

**https://github.com/jmwri/pubg-php**

This package is a wrapper around [PUBG Tracker's API](https://pubgtracker.com/site-api).

Please obide by the rate limits specified by PUBG Tracker.

# Getting started
## Installation
    composer require jmwri/pubg-php
    
## API key
You will need to get an API key from [PUBG Tracker](https://pubgtracker.com/site-api).

# Usage
## Get account
```php
$pubg = new \JmWri\Pubg\Pubg('my-api-key');
$pubg->getAccount(1234567890); // \JmWri\Pubg\Output\Account
```

## Get player stats
```php
$pubg = new \JmWri\Pubg\Pubg('my-api-key');
$report = $pubg->getPlayerStats('test_nickname'); // \JmWri\Pubg\Output\Stats\Report
$report->getStats('eu', 'solo'); // \JmWri\Pubg\Output\Stats\Stat[]
$report->getStats('eu', ['solo', 'duo']); // \JmWri\Pubg\Output\Stats\Stat[]
$report->getStats(['eu', 'na'], 'duo'); // \JmWri\Pubg\Output\Stats\Stat[]
$report->getMatchHistory(); // \JmWri\Pubg\Output\Stats\MatchHistory[]
```

# Support
https://github.com/jmwri/pubg-php/issues
