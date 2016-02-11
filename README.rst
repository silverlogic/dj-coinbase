===================
dj-coinbase
===================

Django + Coinbase made easy


Quick Start
------------

Install dj-coinbase:

.. code-block:: bash

    pip install dj-coinbase

Add djcoinbase to your INSTALLED_APPS:

.. code-block:: python

   INSTALLED_APPS = [
       ...
       'djcoinbase'
       ...
   ]

Add your coinbase API environment, key, secret, and notification secret:

.. code-block:: python

   DJCOINBASE_ENVIRONMENT = 'sandbox'
   DJCOINBASE_API_KEY = '<your api key>'
   DJCOINBASE_API_SECRET = '<your api secret>'
   DJCOINBASE_NOTIFICATION_SECRET = '<anything you want>'

Add to your urls.py:

.. code-block:: python

   url(r'^coinbase/', include('djcoinbase.urls')),

Add the notification endpoint to your coinbase API key settings:

.. image:: http://i.imgur.com/GGalnrY.png

Migrate your database

.. code-block:: bash

   ./manage.py migrate
