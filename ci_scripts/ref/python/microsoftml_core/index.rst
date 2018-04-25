===================
PyTLC
===================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

Getting Started
===============

``PyTLC`` is a powerful machine learning library designed for
interoperability with **scikit-learn** estimators and transforms, while adding a
suite of highly optimized algorithms written in C# for speed and performance. In
addition to the following data structures supported by **scikit-learn** 

   *  ``numpy.ndarray`` and 
   * ``scipy.sparse_cst`` matrices 
   
``PyTLC`` estimators and transforms also support the following as
valid input data for the ``fit()`` and ``transform()`` methods.

   * data stored in ``pandas.DataFrame``
   * data stored in text files
   
This allows additional support for popularly used data structures, as well as
provides ability to stream data from files without loading the entire dataset
into memory, which is beneficial for large datasets.

Documentation
=============

.. toctree::
    :maxdepth: 5
    
    overview
    installationguide
    concepts
    modules
    

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. rxkeywords:: main page, home
