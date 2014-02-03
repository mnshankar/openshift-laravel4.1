Openshift-Laravel
=================

Use this repo to instantly create a Laravel 4.1 application on Openshift (https://www.openshift.com/)

Why Openshift is awesome for Laravel
------------------------------------
1. Free PaaS hosting for trying out code
2. Git push support
3. Full ssh access
4. Ability to schedule cron jobs and setup deploy hooks
5. Easy to scale up

This repository will help you clone laravel 4.1 to your openshift gear with almost zero effort! It takes care of all the minutae involved in setup:

1. requirement of php directory (using symlink)
2. Composer installation (via hooks)
3. Dependency installation in the correct folder (composer install)
4. Using latest version of laravel (4.1.18 as of this writing)

How to use
----------

1. Log into your Openshift account
2. Under the "Applications tab", click on "New Application"
3. Select PHP 5.3 cartridge (or php 5.3 with Zend Server)
4. In the source code field, put in the address of this repository (https://github.com/mnshankar/openshift-laravel4.1)
5. Click on "Create Application"
6. Once your app is started, click on its url and you should see the Laravel welcome page!

NOTE
----
1. When creating your application in *Remember to select php 5.3*. The php 5.4 options that are currently available DO NOT have mcrypt bundled in them and so laravel will fail!

2. When cloning the repo to your local folder for development, bring down the package like so. The "laravel" folder can then be edited to contain your application logic:

```
git clone ssh://52ebddf14rtrec862e000040@php-mnshankar.rhcloud.com/~/git/php.git/
```

Credits
-------
This repo is based on https://github.com/Fale/openshift-laravel4-quickstart
