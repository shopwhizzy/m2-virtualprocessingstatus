# Magento 2 Module MgtWizards VirtualProcessingStatus

    ``mgtwizards/module-virtualprocessingstatus``

-   [Main Functionalities](#markdown-header-main-functionalities)
-   [Installation](#markdown-header-installation)
-   [Configuration](#markdown-header-configuration)
-   [Specifications](#markdown-header-specifications)

## Main Functionalities

When creating invoice, manually or automatically, it observes if order has at least one virtual product, and if is then case, will set order in "processing" status instead of "completed".

Send us an email requesting the module https://shopwhizzy.com/help-center/

Free of charge.

## Installation

\* = in production please use the `--keep-generated` option

### Type 1: Zip file

-   Unzip the zip file in `app/code/MgtWizards/VirtualProcessingStatus`
-   Enable the module by running `php bin/magento module:enable MgtWizards_VirtualProcessingStatus`
-   Apply database updates by running `php bin/magento setup:upgrade`\*
-   Flush the cache by running `php bin/magento cache:flush`

## Configuration

Important: Order status "processing" must be attached to order state "completed" as a pre-condition to make this module works.
![alt text](https://i.imgur.com/WVUecN6.png)

## Specifications

-   Observer
    -   sales_order_invoice_save_after > MgtWizards\VirtualProcessingStatus\Observer\Sales\OrderInvoiceSaveAfter
