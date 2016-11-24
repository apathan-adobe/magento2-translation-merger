# Magento 2 Translations Merger
Merge translations from magento i18n:collect command result with current theme translations. So each time you add some new translatable strings into your templates, you will be able to update your theme/module translation files automatically by running:

Example:

##### php bin/magento i18n:collect-phrases --output "app/i18n/Vendorname/sv_SE/sv_SE.csv" --magento

##### php bin/magento translation-merger:merge app/i18n/Vendorname/sv_SE/ app/design/frontend/Yourtheme/Yourthemepackage/i18n/ sv_SE

This module fix magento issue then running bin/magento i18n:pack , for some reason it just replaces your current theme/module csv translations and not merges them.


# Installation
Add this to your composer.json
```json
  "require-dev": {
        "sensejus/magento2-translation-merger":"dev-master"
    }
```   

Run

  composer update
