# Using the BitPay plugin for WordPress (WP) eCommerce

## Prerequisites

* Last Cart Version Tested: Wordpress 4.0 WP e-commerce 3.8.14.3

You must have a BitPay merchant account to use this plugin.  It's free to [sign-up for a BitPay merchant account](https://bitpay.com/start).


## Installation of .zip file downloaded from bitpay.com

- Install the WP eCommerce plugin from the WordPress Plugin Directory here: https://wordpress.org/plugins/wp-e-commerce/. This payment method requires the WP eCommerce plugin to function because this BitPay file is an extension to the WP eCommerce plugin itself.
- Don't attempt to install this BitPay file through the WordPress plugins control panel. 
- Extract the contents of the zip file.
- Copy the wpsc-merchants folder and paste it into your active WP eCommerce instance (ie `/var/www/html/wordpress/wp-content/plugins/wp-e-commerce`).

## Installation From GitHub

- Install the WP eCommerce plugin from the Wordpress Plugin Directory here: https://wordpress.org/plugins/wp-e-commerce/. This payment method requires the WP eCommerce plugin to function because this BitPay file is an extension to the WP eCommerce plugin itself.
- Don't attempt to install this BitPay file through the WordPress plugins control panel. 
- Clone this repository anywhere onto your server.
- Open up your Terminal
- Change directory into the repository folder that was cloned.
- Once you are inside the repository folder input ./setup username password
- Replace username with your mysql database username that has access to all tables and replace password with the database password.
- Once you run this a folder should show up called wpsc-merchants in the repository directory.
- Copy and Paste content of `src` into your active WP eCommerce instance (ie `/var/www/html/wordpress/wp-content/plugins/wp-e-commerce/wpsc-merchants`).

## Configuration

* Log into the WordPress admin panel, click Settings > Store > Payments (assuming you've already installed WP eCommerce plugin).

* Check the BitPay payment option to activate it and click Save Changes below.

![BTC Invoice](https://raw.githubusercontent.com/aleitner/aleitner.github.io/master/wordpress-ecommerce-plugin-v2/images/Screen%20Shot%202014-11-17%20at%201.03.18%20PM.png)

* Click Settings below the BitPay payment option.

* Edit Display Name if desired.

![BTC Invoice](https://raw.githubusercontent.com/aleitner/aleitner.github.io/master/wordpress-ecommerce-plugin-v2/images/Screen%20Shot%202014-11-17%20at%201.07.14%20PM.png)

* Create a Pairing Code at bitpay.com if you haven't already and set Pairing Code to this value.
  * If you are using a code from **bitpay.com** set the dropdown next to Pairing Code input to **Live**.
  * If you are using a pairing code from **test.bitpay.com** set the dropdown next to the Pairing Code input to **Test**.
* Click Generate to pair with BitPay and create a token for doing transactions.

![BTC Invoice](https://raw.githubusercontent.com/aleitner/aleitner.github.io/master/wordpress-ecommerce-plugin-v2/images/Screen%20Shot%202014-11-17%20at%201.05.54%20PM.png)

* You should now see a paired token in your settings. 

![BTC Invoice](https://raw.githubusercontent.com/aleitner/aleitner.github.io/master/wordpress-ecommerce-plugin-v2/images/Screen%20Shot%202014-11-17%20at%201.06.23%20PM.png)

* Change the Transaction Speed if desired.  Can be `high`, `medium`, or `low`.  HIGH speed confirmations typically take 5-10 seconds, and can be used for digital goods or low-risk items. LOW speed confirmations take about 1 hour, and should be used for high-value items.

![BTC Invoice](https://raw.githubusercontent.com/aleitner/aleitner.github.io/master/wordpress-ecommerce-plugin-v2/images/Screen%20Shot%202014-11-17%20at%201.06.38%20PM.png)

* Input a URL to redirect customers after they have paid the invoice (Transaction Results page, Your Account page, etc.)

![BTC Invoice](https://raw.githubusercontent.com/aleitner/aleitner.github.io/master/wordpress-ecommerce-plugin-v2/images/Screen%20Shot%202014-11-17%20at%201.07.07%20PM.png)

* Click Update below.

## Usage

- Once the configuration is done, whenever a buyer selects Bitcoins as their payment method an invoice is generated at bitpay.com
- The Enable for All button allows other admins on your site to see and edit the token you paired.
- The Disable for All button makes the token pair invisible to all users except for the one who paired the token.
