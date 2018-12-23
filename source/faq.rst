.. _faq:

FAQ
===

Q: How do fecon235 and fecon236 differ?
---------------------------------------

The tools for financial economics started out as IPython notebooks at
**fecon235** https://github.com/rsvp/fecon235 in 2014. Four years later
the source code derived from the patterns and idioms used in rebranded
Jupyter notebooks was refactored at **fecon236**
https://github.com/MathSci/fecon236 and integration tested under both
python27 and python3.

The two repositories are curated wrappers over the Python and Jupyter
ecosystems. The notebooks will be continue to be developed in the
fecon235 ``nb`` directory https://git.io/fecon235nb serving as usage
examples and templates for research, while the source code behind the
notebooks will be supported at fecon236.

Q: How do I INSTALL and start using fecon235?
---------------------------------------------

First: fork, clone, or download a copy of our
`project <https://github.com/rsvp/fecon235>`__ from GitHub.

-  Info on HOWTO fork: https://guides.github.com/activities/forking
-  Info on HOWTO clone:
   https://help.github.com/articles/cloning-a-repository
-  Get zip file without git:
   https://github.com/rsvp/fecon235/zipball/master

Second: our project has external package dependencies which can be
easily fulfilled by `Anaconda <https://www.anaconda.com/download>`__. If
you are new to the Python ecosystem, we would highly recommend that free
distribution which includes Jupyter, IPython, numpy, pandas, matplotlib,
etc.

Optional: to run *old* fecon235 code make sure your local fecon235 top
directory is under the scope of your PYTHONPATH, a system variable.
PYTHONPATH is used by the Python interpreter to determine which modules
to load.

The most important fecon235 assets are the **notebooks** located in the
`nb directory <https://git.io/fecon235nb>`__ (which is explicitly *not*
a package). Please see the introductory notebook at
https://git.io/fecon-intro to get started.

Q: How do I INSTALL and run fecon236?
-------------------------------------

Ideally, fork, clone, or download a copy of our
`project <https://github.com/MathSci/fecon236>`__ from GitHub. A fork
will allow you to later make pull requests. Community development of the
code is an important aspect of the project.

-  Note that fecon236 includes a setup.py file for manual installation.
-  Extra fine details on `fecon236
   installation <https://git.io/236inst>`__
-  Get zip file without git:
   https://github.com/MathSci/fecon236/zipball/master

OK, but there is also the quick way: ``pip install --pre fecon236``

The ``--pre`` flag will include the latest version which is stable
enough for the non-developer user. Of course, it can be used in
conjunction with the ``--upgrade`` flag. To remove the project
completely: ``pip uninstall fecon236``

As for satisfying external dependencies, we recommend the
`Anaconda <https://www.anaconda.com/download>`__ distribution which
properly handles binaries (for computational speed, e.g. MKL Math Kernel
Library) for all operating systems, and correctly performs dependency
resolution (unlike PyPI). Pro tip: get the conda-aware version of pip by
``conda update pip`` before pip-installing fecon236.

If you insist on satisfying the dependencies manually, we have provided
information for a proven deterministic build via
`required.txt <https://git.io/236req>`__

One everything is installed, only one further command suffices:
``import fecon236 as fe``

We adopted absolute\_import throughout this project, which is a feature
compatible with python27, also making fecon236 easy to incorporate into
other projects.

Q: Where is the documentation?
------------------------------

The most current user documentation can be found in the ``docs``
directory, however, the source code is thoroughly documented with useful
comments.

The best way to learn about the user-friendly code is to pick a Jupyter
notebook on a topic which interests you, and then to work interactively
with it for analysis, see the `nb
directory <https://git.io/fecon235nb>`__.

Q: Are there online discussions? Help?
--------------------------------------

Chat with fellow users at Gitter: https://gitter.im/rsvp/fecon235 or
with fellow developers at Gitter: https://gitter.im/MathSci/fecon236

Q: How do I report a bug, or suggest enhancements?
--------------------------------------------------

Chat with us first, then also check the Issues section of repositories.

Q: How do I retrieve economic off-beat FRED data series?
--------------------------------------------------------

To access data from the U.S. Federal Reserve Bank, each economic time
series and its frequency has its own "fredcode" which is freely
available at their site `FRED <https://fred.stlouisfed.org>`__.

::

        df = fe.get( fredcode )
        #            fredcode is entered as a string, or an
        #            assigned variable named d4*, m4*, q4*.
        #  E.g. the variable q4gdpusr contains the string 'GDPC1'
        #       which is U.S. real GDP in 2009 USD billions, SA quarterly.
        fe.plot(df)
        #       df is automatically in pandas DataFrame format.

Q: How do I retrieve data from Quandl?
--------------------------------------

The same idea as FRED above. For example, d7xbtusd='BCHAIN/MKPRU' which
is for the Bitcoin price in USD (d7 indicates that the data is 7 days
per week). The quandlcodes can be found at
`Quandl <https://www.quandl.com>`__, however, use Google search with
keyword "quandl" for better results.

Q: How do I retrieve data series for equities?
----------------------------------------------

We use a special string called "*stock slang*" in the format "s4symbol"
where symbol is spelled out in all lower-case.

For example, to retrieve SPY (the ETF for S&P500), use "s4spy" and this
line to get a pandas DataFrame: ``df = fe.get("s4spy")``

Note: there has recently been upstream disruption in getting equities
data, please consult
`235is7 <https://github.com/rsvp/fecon235/issues/7>`__ for remedies.

Q: Where is the package map for fecon236?
-----------------------------------------

.. ipython:: python

    import fecon236 as fe
    print(fe.map)

