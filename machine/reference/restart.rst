.. -*- coding: utf-8 -*-
.. URL: https://docs.docker.com/machine/reference/restart/
.. SOURCE: https://github.com/docker/machine/blob/master/docs/reference/restart.md
   doc version: 1.10
      https://github.com/docker/machine/commits/master/docs/reference/restart.md
.. check date: 2016/03/09
.. Commits on Feb 21, 2016 d7e97d04436601da26d24b199532652abe78770e
.. ----------------------------------------------------------------------------

.. restart

.. _machine-restart:

=======================================
restart
=======================================

.. code-block:: bash

   Usage: docker-machine restart [arg...]
   
   Restart a machine
   
   Description:
      Argument(s) are one or more machine names.

.. Restart a machine. Oftentimes this is equivalent to docker-machine stop; docker-machine start.

マシンを再起動します。これは ``docker-machine stop; docker-machine start`` の実行と同等です。

.. code-block:: bash

   $ docker-machine restart dev
   Waiting for VM to start...

