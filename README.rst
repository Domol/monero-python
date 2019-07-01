Python Monero module
====================

|travis|_ |coveralls|_


.. |travis| image:: https://travis-ci.org/python-monero/monero-python.svg
.. _travis: https://travis-ci.org/python-monero/monero-python


.. |coveralls| image:: https://coveralls.io/repos/github/python-monero/monero-python/badge.svg
.. _coveralls: https://coveralls.io/github/python-monero/monero-python


This is a fork of `Monero Python`_, a comprehensive Python module for handling
Monero cryptocurrency. The current purpose is to include changes and features
that by design are not included on the original project.

This fork contains the following changes:

* Dropped support for python 2.
* Added: ``get_unspent_outputs`` and ``get_incoming_transactions`` to the wallet.
* Added: ``address_index`` to instances of ``SubAddress``.
* Added: optional ``timeout`` to ``JSONRPCWallet`` and ``JSONRPCDaemon``.  Please note that
  a timeout does not mean that the underlying operation was not executed.
* Added: ``get_transfer`` method to the wallet, allowing users to fetch a single
  transfer by its id.

For documentation about how to use the package please check the original repository.

.. _`Monero Python`: https://github.com/monero-ecosystem/monero-python

Copyrights
----------

Released under the BSD 3-Clause License. See `LICENSE.txt`_.

Copyright (c) 2019 Contributors of this fork: `lalvarezguillen`_, `dethos`_, `Domol`_.

Copyright (c) 2017-2019 Michał Sałaban <michal@salaban.info> and Contributors: `lalanza808`_, `cryptochangements34`_, `atward`_, `rooterkyberian`_, `brucexiu`_,
`lialsoftlab`_, `moneroexamples`_.

Copyright (c) 2016 The MoneroPy Developers (``monero/base58.py`` and ``monero/ed25519.py`` taken from `MoneroPy`_)

Copyright (c) 2011 thomasv@gitorious (``monero/seed.py`` based on `Electrum`_)

.. _`LICENSE.txt`: LICENSE.txt
.. _`MoneroPy`: https://github.com/bigreddmachine/MoneroPy
.. _`Electrum`: https://github.com/spesmilo/electrum

.. _`lalanza808`: https://github.com/lalanza808
.. _`cryptochangements34`: https://github.com/cryptochangements34
.. _`atward`: https://github.com/atward
.. _`rooterkyberian`: https://github.com/rooterkyberian
.. _`brucexiu`: https://github.com/brucexiu
.. _`lialsoftlab`: https://github.com/lialsoftlab
.. _`moneroexamples`: https://github.com/moneroexamples
.. _`lalvarezguillen`: https://github.com/lalvarezguillen
.. _`dethos`: https://github.com/dethos
.. _`Domol`: https://github.com/Domol

Development
-----------

1. Clone the repo
2. Create virtualenv & activate it

.. code-block:: bash

    python3 -m venv .venv
    source .venv/bin/activate

3. Install dependencies

.. code-block:: bash

    pip install -r requirements.txt -r test_requirements.txt

4. Do your thing

5. Run tests

.. code-block:: bash

    pytest
