<p align="center">
    <img src="https://raw.githubusercontent.com/dperkosan/files/master/eshop.jpg" />
</p>

<h1 align="center">Headless E-shop</h1>

For Headless E-shop part is used [**Sylius Standard Edition**](https://github.com/Sylius/Sylius-Standard) + [**Sylius Vue Storefront Plugin**](https://github.com/BitBagCommerce/SyliusVueStorefrontPlugin).

System Requirements
-----

* [Requirements for running Symfony](http://symfony.com/doc/current/reference/requirements.html)
* The recommended operating systems for running Sylius are the Unix systems - Linux, MacOS
* In the production environment recommendation is Apache web server ≥ 2.2, while developing the recommended way to work is to use PHP’s built-in web server
* PHP version: ^7.2
* PHP extensions: `gd`, `exif`, `fileinfo`, `intl`
* PHP configuration settings: `memory_limit ≥ 1024M`, `date.timezone` Use your local timezone
* MySQL	5.7+, 8.0+

Installation
------------

```bash
$ git clone git@github.com:dperkosan/eshop.git
$ cd eshop
```

Please, contact me for:
* DB
* media folder
* jwt folder
* .env.local file

```bash
$ composer install
$ yarn install
$ yarn build
$ symfony serve
$ open http://127.0.0.1:8000/admin/login
```

You can populate ES with this command (in project root folder):

```bash
$ php bin/console app:datapump
```

Tasks
---------------

- [x] Move "Shop Api Plugin" into project
- [x] Creating of "Data pump" in "Sylius" that will copy data from MySql into Elasticsearch
- [ ] Creating platform for "Sylius" in "Storefront API"
- [ ] Synchronisation between MySql and Elasticsearch (on every create, insert, update and delete)
- [ ] Disable front shop
- [ ] Custom functionalities regarding ongoing project