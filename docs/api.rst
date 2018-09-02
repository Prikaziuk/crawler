Crawler Python API
===================

Getting started with Crawler is easy.
The main class you need to care about is

.. autoclass:: crawler.main.Crawler



.. automodule:: crawler.main

.. automodule:: crawler.utils

.. autofunction:: crawler.utils.should_ignore


.. testsetup::

    from crawler.utils import should_ignore
    from crawler.utils import log

.. doctest::

    >>> should_ignore(['blog/$'], 'http://ericholscher.com/blog/')
    True

    >>> should_ignore(['home'], 'http://ericholscher.com/blog/')
    False

    >>> log('http://ericholscher.com/blog/', 200)
    OK: 200 http://ericholscher.com/blog/

    >>> log('http://ericholscher.com/blog/', 500)
    ERR: 500 http://ericholscher.com/blog/

Other directive is ``testcode``

.. testcode::

    log('http://ericholscher.com/blog/', 500)

That requires separate ``testoutput``

.. testoutput::

    ERR: 500 http://ericholscher.com/blog/


If i add this text and push will it automatically appear in the docs?