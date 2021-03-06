# chubbyphp-clean-directories

[![Build Status](https://api.travis-ci.org/chubbyphp/chubbyphp-clean-directories.png?branch=master)](https://travis-ci.org/chubbyphp/chubbyphp-clean-directories)
[![Coverage Status](https://coveralls.io/repos/github/chubbyphp/chubbyphp-clean-directories/badge.svg?branch=master)](https://coveralls.io/github/chubbyphp/chubbyphp-clean-directories?branch=master)
[![Latest Stable Version](https://poser.pugx.org/chubbyphp/chubbyphp-clean-directories/v/stable.png)](https://packagist.org/packages/chubbyphp/chubbyphp-clean-directories)
[![Total Downloads](https://poser.pugx.org/chubbyphp/chubbyphp-clean-directories/downloads.png)](https://packagist.org/packages/chubbyphp/chubbyphp-clean-directories)
[![Monthly Downloads](https://poser.pugx.org/chubbyphp/chubbyphp-clean-directories/d/monthly)](https://packagist.org/packages/chubbyphp/chubbyphp-clean-directories)
[![Daily Downloads](https://poser.pugx.org/chubbyphp/chubbyphp-clean-directories/d/daily)](https://packagist.org/packages/chubbyphp/chubbyphp-clean-directories)

## Description

A command to clean directories based on directoryName => directoryPath mapping.

## Requirements

 * php: ^7.2
 * [symfony/console][2]: ^3.4|^4.4|^5.1

## Installation

Through [Composer](http://getcomposer.org) as [chubbyphp/chubbyphp-clean-directories][1].

```sh
composer require chubbyphp/chubbyphp-clean-directories "^1.0"
```

## Usage

```php
#!/usr/bin/env php
<?php

declare(strict_types=1);

namespace App;

use Chubbyphp\CleanDirectories\Command\CleanDirectoriesCommand;
use Symfony\Component\Console\Application;
use Symfony\Component\Console\Command\Command;
use Symfony\Component\Console\Input\ArgvInput;
use Symfony\Component\Console\Input\InputOption;

require __DIR__.'/../vendor/autoload.php';

$input = new ArgvInput();

$console = new Application();
$console->addCommand(new CleanDirectoriesCommand(['directoryName' => 'directoryPath']));
$console->run($input);
```

```sh
console clean-directories directoryName
```

## Copyright

Dominik Zogg 2020

[1]: https://packagist.org/packages/chubbyphp/chubbyphp-clean-directories
[2]: https://packagist.org/packages/symfony/console
