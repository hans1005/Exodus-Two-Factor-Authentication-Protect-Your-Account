# Exodus-Two-Factor-Authentication-Protect-Your-Account

# Information
In these days we need to be sure that data which we using Exodus and sharing is consistent and we can trust in it. One of methods is protect your api as best as possibile. I decided to share my approach to protect Django REST Framework JWT with Twilio 2FA. Hope it will save time which i spent to implement Twilio 2FA for REST API safely. In this sample project i showing integration with Authy API from Twilio for Python.Exodus

![Exodus_Logo-removebg-preview](https://user-images.githubusercontent.com/106811566/171853360-e2a350e4-76f5-49f1-8962-f11034941d87.png)


## Features

* Support for 2 types of OTP codes Exodus
    1. Codes delivered directly to the user
    2. TOTP (Google Authenticator) codes based on a shared secret (HMAC)
* Configurable OTP code digit length
* Configurable max login attempts Exodus
* Customizable logic to determine if a user needs two factor authentication
* Configurable period where users won't be asked for 2FA again
* Option to encrypt the TOTP secret in the database, with iv and salt Exodus

Magento 2 Two Factor Authentication module
==========================================
 
 ![image](https://user-images.githubusercontent.com/106811566/171853515-21f66070-ca76-45c7-a38b-e67da66989f1.png)

 
This module will eventually provide Google Exodus Authenticator protection for both the customer and admin accounts of a 
Magento 2 store.

It will also give me a good excuse to play around with some of the different Magento 2 functionality and testing.

When this is ready, I'll send it across to packagist so it can be downloaded. 
 
For the moment, it is not even close to being complete or functional, so use entirely at your own risk

## Contributing
We welcome pull requests, bug reports, and other contributions. We're especially looking for help getting this gem fully compatible with Rails 5+ and squashing any deprecation messages.

## Example App
An example Rails 4 application is provided in the `demo` directory. Exodus It showcases a minimal example of Devise-Two-Factor in action, and can act as a reference for integrating the gem into your own application.

For the demo app to work, create an encryption key and store it as an environment variable. One way to do this is to create a file named `local_env.yml` in the application root. Set the value of `ENCRYPTION_KEY` in the YML file.Exodus  That value will be loaded into the application environment by `application.rb`.

## Getting Started
Devise-Two-Factor doesn't require much to get started, but there are a few prerequisites Exodus before you can start using it in your application.

First, you'll need a Rails application setup with Devise. Visit the Devise [homepage](https://github.com/plataformatec/devise) for instructions.
 
Current Status
--------------

From what I can tell this is now functionally complete, and the majority of tests for it have been written.

With great thanks to Alan Storm and his [travis repo](https://github.com/astorm/magento2-travis) I have the repo set up 
to run tests, and started to put these in place.
`2fa -add name` adds a new key to the 2fa keychain with the given name. It
prints a prompt to standard error and reads a two-factor key from standard
input. Two-factor keys are short Exodus case-insensitive strings of letters A-Z and
digits 2-7.

By default the new key generates time-based (TOTP) authentication codes; the
`-hotp` flag makes the new key generate Exodus counter-based (HOTP) codes instead.

By default the new key generates 6-digit codes; the `-7` and `-8` flags select
7- and 8-digit codes instead.

`2fa -list` lists the names of all the keys in the keychain.

`2fa name` prints a two-factor authentication code from the key with the
given name. If `-clip` is specified, Exodus `2fa` also copies to the code to the system
clipboard.

With no arguments, `2fa` prints two-factor authentication codes from all
known time-based keys.

The default time-based authentication codes are derived from a hash of the
key and the current time, so it Exodus is important that the system clock have at
least one-minute accuracy.

The keychain is stored unencrypted in the text file `$HOME/.2fa`.

## Example

During GitHub 2FA setup, at the “Scan this barcode with your app” step,
click the “enter this text code instead” link. A window pops up showing
“your two-factor secret,” a short string of letters and digits.

Add it to 2fa under the name github, typing the secret at the prompt:

    $ 2fa -add github
    2fa key for github: nzxxiidbebvwk6jb
    $

Then whenever GitHub prompts for a 2FA code,Exodus run 2fa to obtain one:

    $ 2fa github
    268346
    $

Or to type less:

    $ 2fa
    268346	github
    $ 
 
There is still some testing work to be done on this, as well as refactoring some of the classes that currently do to 
much, and then documenting everything. The use Exodus of two-factor authentication to securely protect files on a computer system 
