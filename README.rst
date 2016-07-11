.. -*- mode: rst -*-

polylearn
=========

A library for higher-order **factorization machines** and **polynomial networks**
for classification and regression in Python.

Factorization machines and polynomial networks are machine learning models
that can capture **feature interaction** (co-occurrence) through polynomial terms.
Because feature interactions can be very sparse, it's common to use **low rank,
factorized representations**; this way, we can learn weights even for feature
co-occurrences that haven't been observed at training time.

Factorization machines are popular for recommender systems, as they are a
generalization of matrix completion models.

This package provides:

- direct coordinate descent algorithm for factorization machines,
- lifted solver for fitting polynomial networks of arbitrary degree,
- `scikit-learn <http://scikit-learn.org>`_-compatible API,
- `Cython <http://cython.org>`_ implementations for computationally intensive parts.

Installation
------------

Binary packages are not yet available.

The development version of polylearn can be installed from its git repository. In
this case it is assumed that you have the git version control system, a working
C++ compiler, Cython, lightning, and the numpy development libraries. In order to
install the development version, type::

   git clone https://github.com/vene/polylearn.git
   cd polylearn
   python setup.py build
   sudo python setup.py install


References
----------

The solvers implemented are introduced in [1]_. Factorization machines are introduced
in [2]_ and polynomial networks in [3]_.

.. [1] Mathieu Blondel, Masakazu Ishihata, Akinori Fujino, Naonori Ueda.
       *Polynomial Networks and Factorization Machines: New Insights and
       Efficient Training Algorithms.*  In: Proc. of ICML 2016.
       [`PDF <http://mblondel.org/publications/mblondel-icml2016.pdf>`_]

.. [2] Steffen Rendle. *Factorization machines.* In: Proc. of IEEE ICDM 2010.
       [`PDF <https://www.ismll.uni-hildesheim.de/pub/pdfs/Rendle2010FM.pdf>`_]

.. [3] Roi Livni, Shai Shalev-Shwartz, Ohad Shamir.
       *On the computational efficiency of training neural networks.*
       In: Proc. of NIPS 2014.
       [`arXiv <http://arxiv.org/abs/1410.1141>`_]

Authors
-------

- Vlad Niculae, 2016-present