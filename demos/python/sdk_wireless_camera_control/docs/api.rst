:github_url: https://github.com/gopro/OpenGoPro/tree/main/demos/python/sdk_wireless_camera_control

Interfaces
**********

This section is a reference for the Open GoPro Python Package API. The BLE / Wifi API's that
this package implements can be found in the Open GoPro documentation linked from :ref:`package summary<Summary>`

.. note::
   Not everything is exposed here. This section should only consist of the interface
   information that a user (not a developer) of the Open GoPro module should care about.

For a higher-level summary / usage, see the :ref:`usage<Usage>` section

.. warning::
   This documentation is not a substitute for the Open GoPro BLE and WiFi
   `specifications <https://gopro.github.io/OpenGoPro/>`_. That is, this interface shows how to use the various
   commands but is not an exhaustive source of information for what each command does. The Open GoPro specs
   should be used simultaneously with this document for development.

GoPro
=====

This can be imported as:

.. code-block:: python

   from open_gopro import GoPro

.. automodule:: open_gopro.gopro
   :members:

API
===

These are both the base types that are used to implement the API (BLE Setting, Ble Status, etc.) and the
version-specific API's themselves.

Since the API is configured (by version) dynamically after a connection is formed, these should not be imported
directly and instead should be accessed using the relevant properties (`ble_command`, `wifi_setting`, etc.) of a
GoPro(:class:`open_gopro.gopro.GoPro`) instance. Doing so will ensure that the correct parameters are selected
and data is sent.

Base Types
----------

These are the base types that are used to implement version-specific API's.

BLE Setting
^^^^^^^^^^^

.. autoclass:: open_gopro.api.builders.BleSetting
   :members:

BLE Status
^^^^^^^^^^

.. autoclass:: open_gopro.api.builders.BleStatus
   :members:

WiFi Setting
^^^^^^^^^^^^

.. autoclass:: open_gopro.api.builders.WifiSetting
   :members:

BLE Commands
------------

.. autoclass:: open_gopro.api.ble_commands.BleCommands
   :members:

BLE Settings
------------

.. autoclass:: open_gopro.api.ble_commands.BleSettings
   :members:

BLE Statuses
------------

.. autoclass:: open_gopro.api.ble_commands.BleStatuses
   :members:

WiFi Commands
-------------

.. autoclass:: open_gopro.api.wifi_commands.WifiCommands
   :members:

WiFi Settings
-------------

.. autoclass:: open_gopro.api.wifi_commands.WifiSettings
   :members:

Parameters
----------

All of these parameters can be accessed via:

.. code-block:: python

   from open_gopro import Params

.. autoclass:: open_gopro.api.params
   :members:
   :undoc-members:

Responses
=========

This can be imported via:

.. code-block:: python

   from open_gopro import GoProResp

.. autoclass:: open_gopro.responses.GoProResp
   :members:


Constants
=========

These can be imported as:

.. code-block:: python

   from open_gopro import constants


.. automodule:: open_gopro.constants
   :members:
   :undoc-members: