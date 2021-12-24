# Magento 2 Module Nosto Puzzle

    ``nosto/module-puzzle``

 - [Main Functionalities](#markdown-header-main-functionalities)
 - [Installation](#markdown-header-installation)
 - [Configuration](#markdown-header-configuration)
 - [Specifications](#markdown-header-specifications)
 - [Attributes](#markdown-header-attributes)


## Main Functionalities
Update product model’s list price and price attributes by taking 10% off the prices if the visitor / client is logged in to Magento store.

## Installation
\* = in production please use the `--keep-generated` option

### Type 1: Zip file

 - Unzip the zip file in `app/code/Nosto`
 - Enable the module by running `php bin/magento module:enable Nosto_Puzzle`
 - Apply database updates by running `php bin/magento setup:upgrade`\*
 - Flush the cache by running `php bin/magento cache:flush`

### Type 2: Composer

 - Make the module available in a composer repository for example:
    - private repository `repo.magento.com`
    - public repository `packagist.org`
    - public github repository as vcs
 - Add the composer repository to the configuration by running `composer config repositories.repo.magento.com composer https://repo.magento.com/`
 - Install the module composer by running `composer require nosto/module-puzzle`
 - enable the module by running `php bin/magento module:enable Nosto_Puzzle`
 - apply database updates by running `php bin/magento setup:upgrade`\*
 - Flush the cache by running `php bin/magento cache:flush`


## Specifications

 - Helper
	- Nosto\Puzzle\Helper\Nosto

 - Observer
	- nosto_product_load_after > Nosto\Puzzle\Observer\Frontend\Nosto\ProductLoadAfter
