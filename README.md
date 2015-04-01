# FTHLC - Simple but fast php web framework

FTHLC Framework - aka. For Those Who Loves C9s Framework - is a simple but
fast web framework for PHP 5.3+.

## Introduction

Tired using fat, slow, nobody-can-read framework like $ymfoning? Use FTHLC and you'll
love it in a second!

FTHLC has exactly zero line of code, which make it be the fastest web framework in the world!
No additional effort, no performance penalty, doing just the thing you want it to do!

We use [Pux](https://github.com/c9s/Pux) for routing, [LazyRecord](https://github.com/c9s/LazyRecord) for ORM and also [CLIFramework](https://github.com/c9s/CLIFramework) to save your life!
Less step, more c9s! It's definitely c9s all-in-one!

## Getting Started

`php composer.phar require ronmi/fthlc`

## Synopsis

Routing:

```php
$mux = new Pux\Mux;
$mux->mount('', (new Your/App/Controller())->expand());
```

Controller:
```php
class YourController extends Pux\Controller
{
    public function indexAction($arg1, $arg2)
    {
        // do something
    }
}
```

Model:
```php
class YourModelSchema extends LazyRecord\Schema
{
    public function schema()
    {
        $this->column('column1')->integer()->default(1);
    }
}
```

and

```sh
vendor/bin/lazy init
vendor/bin/lazy conf
vendor/bin/lazy build-schema
vendor/bin/lazy create-db
vendor/bin/lazy sql

vendor/bin/lazy migrate
```

Command line interface:
```php
class YourCLICommand extends CLIFramework\Command
{
    public function brief() {
        return 'Only for test.';
    }
    public function arguments($args)
    {
        $args->add('arg1');
    }
    public function execute($arg1)
    {
        $this->logger->info($arg1);
    }
}
```

## Testimonials

* We have 3141.59% speed boost after changing from $ymfoning to FTHLC. _bill.doors@m1cr0s0f7.com_
* Fast, fast, and faster! _larry.chapter@goodle.com_
* I will never use any other framework! _jeff.bagels@mamasong.com_
* 用了它之後，我感覺自己變聰明了，考試都考一百分呢！ _60cm@gg-in.in_