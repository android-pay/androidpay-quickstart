# androidpay-quickstart-cybs

## Overview
This is a fork of the official Google Android Pay quickstart app, which demonstrates basic functionality of the API.
It has been modified to return data in a format appropriate for use with the CyberSource payment gateway. 

# Android Pay official tutorial
https://developers.google.com/android-pay/android/tutorial

# CyberSource Android Pay documentation
https://www.cybersource.com/products/payment_processing/android_pay/

## Requirements
Run the Android SDK Manager (`android sdk`) and ensure that you have the following installed:

  * Android SDK Build-tools 22.0.1
  * Google Play services version 25
  * Android Support Library version 22.2
  * Android Support Repository version 15
 
Ensure you have a CyberSource test account created.  If not, do so using this link:
https://www.cybersource.com/register

## Generating a Public Key
This sample assumes that you intend to use Android Pay with the goal of processing on the CyberSource payment gateway.
As such, you will need to generate a public key and use it to obtain a blob from the Android Pay service.
This blob is then prepared with additional data elements, where it can be forwarded to CyberSource using the 
standard API.  For more information on this part, contact CyberSource.

To obtain your public key:

  * Access the CyberSource Business Center (https://ebctest.cybersource.com)  
  * Login as an administrator.
  * Navigate to Account Management -> Digital Payment Solutions.
  * Click on the Android Pay solution icon.
  * Generate a new public key using the on-screen button.

The key should look something like this:

`MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAE7ILxwCqeus7ZfI9nlxF6op9zyliPjHm35J14Mg4TQJFi8HCsTWqtVM5CDfijze8+rdmLvCBj3mNNnwcXZ47V9w==`

Place this key into `app/src/main/res/values/ids.xml`

This application is intended as an example of how to integrate with the CyberSource system. It is not endorsed by, affiliated with, or supported by CyberSource.  
