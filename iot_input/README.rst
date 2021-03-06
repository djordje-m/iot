=========
IoT Input
=========

.. !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fiot-lightgray.png?logo=github
    :target: https://github.com/OCA/iot/tree/12.0/iot_input
    :alt: OCA/iot
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/iot-12-0/iot-12-0-iot_input
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runbot-Try%20me-875A7B.png
    :target: https://runbot.odoo-community.org/runbot/269/12.0
    :alt: Try me on Runbot

|badge1| |badge2| |badge3| |badge4| |badge5| 

This addon allows to use a device in order to input data to odoo automatically.

It opens a URL that a device can use to connect (with a password) that can only
execute an specific action.

Inputs are useful when a device wants to communicate to odoo for a single
and simple action.
This way, the device does not need to be configured with a odoo user and
password, it is handled by odoo devices.

Examples:

* Sending the temperature every three minutes.
* Sending the RFID that the device has received in order to perform some action

**Table of contents**

.. contents::
   :local:

Usage
=====

1. Create a Device on `IoT > Config Devices`
2. Access the Inputs section of the device
3. Create an input. You must define a serial, passphrase, function and model

The function that the system will call must be of the following kind::

    @api.model
        def call_function(self, key):
        return {}

Where `key` is the input string send by the device and the result must be a dictionary
that will be responded to the device as a JSON.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/iot/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed
`feedback <https://github.com/OCA/iot/issues/new?body=module:%20iot_input%0Aversion:%2012.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Creu Blanca

Contributors
~~~~~~~~~~~~

* Enric Tobella <etobella@creublanca.es>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

.. |maintainer-etobella| image:: https://github.com/etobella.png?size=40px
    :target: https://github.com/etobella
    :alt: etobella

Current `maintainer <https://odoo-community.org/page/maintainer-role>`__:

|maintainer-etobella| 

This module is part of the `OCA/iot <https://github.com/OCA/iot/tree/12.0/iot_input>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
