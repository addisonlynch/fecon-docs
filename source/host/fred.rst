.. _fred:

FRED
====

Overview
--------

Contents
~~~~~~~~

- :ref:`fred.codes`
- :ref:`fred.helpers`
- :ref:`fred.utilities`

About
~~~~~

.. automodule:: fecon236.host.fred


.. _fred.codes:

FRED Series Codes
-----------------

.. _fred.codes.libor:

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


.. _fred.codes.fedfunds:

Federal Funds Rate
~~~~~~~~~~~~~~~~~~

``DFF``
^^^^^^^

Effective Federal Funds Rate, Daily since 1954

**Frequency: Daily**

**Period: 1954-present**

.. _fred.codes.treasurybills:

Treasury Bills
~~~~~~~~~~~~~~

``DTB3``
^^^^^^^^

3-Month Treasury Bill: Secondary Market Rate

**Frequency: Daily**

**Period: 1954-present**


.. _fred.helpers:

FRED Helper Codes
-----------------

FRED helper codes can be obtained from ``fecon236.host.fred``:

.. ipython:: python

    from fecon236.host.fred import d4ff30, getfred

    getfred(d4ff30)


.. fred.helpers.fedfunds:

Federal Funds Rate
~~~~~~~~~~~~~~~~~~

``d4ff30``
^^^^^^^^^^

Synthetic Federal Funds Rate, using the 30-day exponential moving average.


.. _fred.utilities:

FRED Utilities
--------------

.. _fred.utilities.resampling:

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


.. _fred.utilities.indexing:

Indexing
~~~~~~~~

.. autofunction:: fecon236.host.fred.index_delta_secs

.. _fred.utilities.io:

I/O
~~~

.. autofunction:: fecon236.host.fred.readfile
