# DesignPatternsPHP

## 日本語翻訳版

[![Build Status](https://travis-ci.org/domnikl/DesignPatternsPHP.svg?branch=master)](https://travis-ci.org/domnikl/DesignPatternsPHP)

[![Documentation Status](https://readthedocs.org/projects/designpatternsphp/badge/?version=latest)](https://readthedocs.org/projects/designpatternsphp/?badge=latest)

[![Donate](https://img.shields.io/badge/donate-paypal-blue.svg?style=flat-square)](https://paypal.me/DominikLiebler)

[Read the Docs of DesignPatternsPHP](http://designpatternsphp.readthedocs.org)
or [Download as PDF/Epub](https://readthedocs.org/projects/designpatternsphp/downloads/)

こちらの資料では知られたデザインパターンといくつかのサンプルコードを、PHP ではどのように実装するのかを記載します。

> This is a collection of known design patterns and some sample code how to implement them in PHP. Every pattern has a small list of examples (most of them from Zend Framework, Symfony2 or Doctrine2 as I'm most familiar with this software).

デザインパータンについては知っていても、アプリケーションの中でどのように適用すればいいのかがよくわかっていないという課題があるように感じます。

> I think the problem with patterns is that often people do know them but don't know when to apply which.

## 導入編

> ## Installation

サンプルコードで何が起きているかを確認するためには実際にテストコードを実行して確認すべきでしょう。
そのために、`composer`を使って依存関係をインストールしてください。

> You should look at and run the tests to see what happens in the example.
> To do this, you should install dependencies with `Composer` first:

```bash
$ composer install
```

`Composer`のインストールの仕方や使い方についてより深く知りたい場合は[ココ](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx)で確認してください。

> Read more about how to install and use `Composer` on your local machine [here](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx).

テストコードでは`phpunit`を実行します。

> To run the tests use `phpunit`:

```bash
$ ./vendor/bin/phpunit
```

## Docker を使う（オプション）

> ## using Docker (optional)

必要に応じて[Docker for Mac, Windows or Linux](https://docs.docker.com/compose/install/)を使用してドキュメントを作成して閲覧することができます。

> You can optionally build and browse the documentation using [Docker for Mac, Windows or Linux](https://docs.docker.com/compose/install/).

実行方法は以下です。

> Just run:

```bash
$ docker-compose up
```

[http://localhost:8080/README.html](http://localhost:8080/README.html)にアクセスすれば、生成されたドキュメントを読むことができます。

> Go to [http://localhost:8080/README.html](http://localhost:8080/README.html) to read the generated documentation.

`docker-compose`を使うためには以下のようにして依存関係をインストールするだけです。

> To only install the dependencies, use `docker-compose` like this:

```bash
$ docker-compose run php php composer.phar install
```

## パターン

> ## Patterns

デザインパターンはだいたい３つのカテゴリで構成されています。
[:notebook:](http://en.wikipedia.org/wiki/Software_design_pattern)をクリックするとすべての例を WikiPedia で確認することができます。

> The patterns can be structured in roughly three different categories. Please click on the [:notebook:](http://en.wikipedia.org/wiki/Software_design_pattern) for a full explanation of the pattern on Wikipedia.

### 作成系

> ### [Creational](Creational)

- [AbstractFactory](Creational/AbstractFactory) [:notebook:](http://en.wikipedia.org/wiki/Abstract_factory_pattern)
- [Builder](Creational/Builder) [:notebook:](http://en.wikipedia.org/wiki/Builder_pattern)
- [FactoryMethod](Creational/FactoryMethod) [:notebook:](http://en.wikipedia.org/wiki/Factory_method_pattern)
- [Multiton](Creational/Multiton) (is considered an anti-pattern! :no_entry:)
- [Pool](Creational/Pool) [:notebook:](http://en.wikipedia.org/wiki/Object_pool_pattern)
- [Prototype](Creational/Prototype) [:notebook:](http://en.wikipedia.org/wiki/Prototype_pattern)
- [SimpleFactory](Creational/SimpleFactory)
- [Singleton](Creational/Singleton) [:notebook:](http://en.wikipedia.org/wiki/Singleton_pattern) (is considered an anti-pattern! :no_entry:)
- [StaticFactory](Creational/StaticFactory)

### 構築系

> ### [Structural](Structural)

- [Adapter](Structural/Adapter) [:notebook:](http://en.wikipedia.org/wiki/Adapter_pattern)
- [Bridge](Structural/Bridge) [:notebook:](http://en.wikipedia.org/wiki/Bridge_pattern)
- [Composite](Structural/Composite) [:notebook:](http://en.wikipedia.org/wiki/Composite_pattern)
- [DataMapper](Structural/DataMapper) [:notebook:](http://en.wikipedia.org/wiki/Data_mapper_pattern)
- [Decorator](Structural/Decorator) [:notebook:](http://en.wikipedia.org/wiki/Decorator_pattern)
- [DependencyInjection](Structural/DependencyInjection) [:notebook:](http://en.wikipedia.org/wiki/Dependency_injection)
- [Facade](Structural/Facade) [:notebook:](http://en.wikipedia.org/wiki/Facade_pattern)
- [FluentInterface](Structural/FluentInterface) [:notebook:](http://en.wikipedia.org/wiki/Fluent_interface)
- [Flyweight](Structural/Flyweight) [:notebook:](https://en.wikipedia.org/wiki/Flyweight_pattern)
- [Proxy](Structural/Proxy) [:notebook:](http://en.wikipedia.org/wiki/Proxy_pattern)
- [Registry](Structural/Registry) [:notebook:](http://en.wikipedia.org/wiki/Service_locator_pattern)

### 行動系

> ### [Behavioral](Behavioral)

- [ChainOfResponsibilities](Behavioral/ChainOfResponsibilities) [:notebook:](http://en.wikipedia.org/wiki/Chain_of_responsibility_pattern)
- [Command](Behavioral/Command) [:notebook:](http://en.wikipedia.org/wiki/Command_pattern)
- [Iterator](Behavioral/Iterator) [:notebook:](http://en.wikipedia.org/wiki/Iterator_pattern)
- [Mediator](Behavioral/Mediator) [:notebook:](http://en.wikipedia.org/wiki/Mediator_pattern)
- [Memento](Behavioral/Memento) [:notebook:](http://en.wikipedia.org/wiki/Memento_pattern)
- [NullObject](Behavioral/NullObject) [:notebook:](http://en.wikipedia.org/wiki/Null_Object_pattern)
- [Observer](Behavioral/Observer) [:notebook:](http://en.wikipedia.org/wiki/Observer_pattern)
- [Specification](Behavioral/Specification) [:notebook:](http://en.wikipedia.org/wiki/Specification_pattern)
- [State](Behavioral/State) [:notebook:](http://en.wikipedia.org/wiki/State_pattern)
- [Strategy](Behavioral/Strategy) [:notebook:](http://en.wikipedia.org/wiki/Strategy_pattern)
- [TemplateMethod](Behavioral/TemplateMethod) [:notebook:](http://en.wikipedia.org/wiki/Template_method_pattern)
- [Visitor](Behavioral/Visitor) [:notebook:](http://en.wikipedia.org/wiki/Visitor_pattern)

### もっと

> ### [More](More)

- [ServiceLocator](More/ServiceLocator) [:notebook:](http://en.wikipedia.org/wiki/Service_locator_pattern) (is considered an anti-pattern! :no_entry:)
- [Repository](More/Repository)
- [EAV](More/EAV) [:notebook:](https://en.wikipedia.org/wiki/Entity%E2%80%93attribute%E2%80%93value_model)

## コントリビュート

> ## Contribute

もし、サンプルコードにバグが見つかったり、翻訳間違いを見つけた場合は、お気軽にフォークして、変更内容のプルリクエストを送ってください。
ただし、コードの一貫性を維持するために、[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) を利用して [PSR2 standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) を実行してください。
実行方法は以下の通りです。
`./vendor/bin/phpcs -p --standard=PSR2 --ignore=vendor .`.

> If you encounter any bugs or missing translations, please feel free to fork and send a pull request with your changes.
> To establish a consistent code quality, please check your code using [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) against [PSR2 standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) using `./vendor/bin/phpcs -p --standard=PSR2 --ignore=vendor .`.
