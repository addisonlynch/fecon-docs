.. _fred:

FRED
====

Overview
--------

Contents
~~~~~~~~

- :ref:`fredcodes`
- :ref:`fredhelpers`
- :ref:`fredutilities`

About
~~~~~

.. automodule:: fecon236.host.fred


.. _fredcodes:

FRED Series Codes
-----------------

.. _fredcodes.libor:

LIBOR
~~~~~

``JPY3MTD156N``
^^^^^^^^^^^^^^^

3-Month London Interbank Offered Rate (LIBOR), based on Japanese Yen

**Frequency: Daily**

**Period: 1986-present**


``EUR3MTD156N``
^^^^^^^^^^^^^^^

3-Month London Interbank Offered Rate (LIBOR), based on Euro

**Frequency: Daily**

**Period: 1986-present**

``USD3MTD156N``
^^^^^^^^^^^^^^^

3-Month London Interbank Offered Rate (LIBOR), based on U.S. Dollar

**Frequency: Daily**

**Period: 1986-present**


.. _fredcodes.fedfunds:

Federal Funds Rate
~~~~~~~~~~~~~~~~~~

``DFF``
^^^^^^^

Effective Federal Funds Rate, Daily since 1954

**Frequency: Daily**

**Period: 1954-present**

.. _fredcodes.treasurybills:

Treasury Bills
~~~~~~~~~~~~~~

``DTB3``
^^^^^^^^

3-Month Treasury Bill: Secondary Market Rate

**Frequency: Daily**

**Period: 1954-present**


.. _fredhelpers:

FRED Helper Codes
-----------------

FRED helper codes can be obtained from ``fecon236.host.fred``:

.. ipython:: python

    from fecon236.host.fred import d4ff30, getfred

    getfred(d4ff30)


.. _fredhelpers.fedfunds:

Federal Funds Rate
~~~~~~~~~~~~~~~~~~

``d4ff30``
^^^^^^^^^^

Synthetic Federal Funds Rate, using the 30-day exponential moving average.


.. _fredutilities:

FRED Utilities
--------------

.. _fredutilities.resampling:

Resampling
~~~~~~~~~~

Daily
^^^^^

.. autofunction:: fecon236.host.fred.daily

Monthly
^^^^^^^

.. autofunction:: fecon236.host.fred.monthly

Quarterly
^^^^^^^^^

.. autofunction:: fecon236.host.fred.quarterly


.. _fredutilities.indexing:

Indexing
~~~~~~~~

.. autofunction:: fecon236.host.fred.index_delta_secs

.. _fredutilities.io:

I/O
~~~

.. autofunction:: fecon236.host.fred.readfile
