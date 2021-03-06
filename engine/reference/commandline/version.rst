.. *- coding: utf-8 -*-
.. URL: https://docs.docker.com/engine/reference/commandline/version/
.. SOURCE: https://github.com/docker/docker/blob/master/docs/reference/commandline/version.md
   doc version: 1.10
      https://github.com/docker/docker/commits/master/docs/reference/commandline/version.md
.. check date: 2016/02/25
.. Commits on Dec 24, 2015 e6115a6c1c02768898b0a47e550e6c67b433c436
.. -------------------------------------------------------------------

.. version

=======================================
version
=======================================

.. code-block:: bash

   Usage: docker version [OPTIONS]
   
   Show the Docker version information.
   
     -f, --format=""    Format the output using the given go template
     --help             Print usage

.. By default, this will render all version information in an easy to read layout. If a format is specified, the given template will be executed instead.

デフォルトでは、全てのバージョン情報を読みやすい形式で表示します。フォーマットが指定されれば、特定のテンプレートで処理されます。

.. Go’s text/template package describes all the details of the format.

Go 言語の `text/template <http://golang.org/pkg/text/template/>`_ パッケージにフォーマットの全ての詳細が記載されています。

.. Examples

例
==========

.. Default output:

**デフォルトの出力：**

.. code-block:: bash

   $ docker version
   Client:
    Version:      1.8.0
    API version:  1.20
    Go version:   go1.4.2
    Git commit:   f5bae0a
    Built:        Tue Jun 23 17:56:00 UTC 2015
    OS/Arch:      linux/amd64
   
   Server:
    Version:      1.8.0
    API version:  1.20
    Go version:   go1.4.2
    Git commit:   f5bae0a
    Built:        Tue Jun 23 17:56:00 UTC 2015
    OS/Arch:      linux/amd64

.. Get server version:

**サーバのバージョンを取得：**

.. code-block:: bash

   $ docker version --format '{{.Server.Version}}'
   1.8.0

.. Dump raw data:

**raw データのダンプ：**

.. code-block:: bash

   $ docker version --format '{{json .}}'
   {"Client":{"Version":"1.8.0","ApiVersion":"1.20","GitCommit":"f5bae0a","GoVersion":"go1.4.2","Os":"linux","Arch":"amd64","BuildTime":"Tue Jun 23 17:56:00 UTC 2015"},"ServerOK":true,"Server":{"Version":"1.8.0","ApiVersion":"1.20","GitCommit":"f5bae0a","GoVersion":"go1.4.2","Os":"linux","Arch":"amd64","KernelVersion":"3.13.2-gentoo","BuildTime":"Tue Jun 23 17:56:00 UTC 2015"}}

