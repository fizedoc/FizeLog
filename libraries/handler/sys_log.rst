============
系统日志
============


::

    系统日志形式日志类


+-------------+-------------------------------------------------+
|属性         |值                                               |
+=============+=================================================+
|命名空间     |fize\\log\\handler                               |
+-------------+-------------------------------------------------+
|类名         |SysLog                                           |
+-------------+-------------------------------------------------+
|父类         |fize\\log\\AbstractLog                           |
+-------------+-------------------------------------------------+
|实现接口     |fize\\log\\LogHandler, Psr\\Log\\LoggerInterface |
+-------------+-------------------------------------------------+


:方法:


+-----------------+--------------------------------------------------------------------------------------------------+
|方法名           |说明                                                                                              |
+=================+==================================================================================================+
|`__construct()`_ |构造函数                                                                                          |
+-----------------+--------------------------------------------------------------------------------------------------+
|`__destruct()`_  |析构函数                                                                                          |
+-----------------+--------------------------------------------------------------------------------------------------+
|`log()`_         |可任意级别记录日志                                                                                |
+-----------------+--------------------------------------------------------------------------------------------------+
|`emergency()`_   |System is unusable.                                                                               |
+-----------------+--------------------------------------------------------------------------------------------------+
|`alert()`_       |Action must be taken immediately.                                                                 |
+-----------------+--------------------------------------------------------------------------------------------------+
|`critical()`_    |Critical conditions.                                                                              |
+-----------------+--------------------------------------------------------------------------------------------------+
|`error()`_       |Runtime errors that do not require immediate action but should typically
be logged and monitored. |
+-----------------+--------------------------------------------------------------------------------------------------+
|`warning()`_     |Exceptional occurrences that are not errors.                                                      |
+-----------------+--------------------------------------------------------------------------------------------------+
|`notice()`_      |Normal but significant events.                                                                    |
+-----------------+--------------------------------------------------------------------------------------------------+
|`info()`_        |Interesting events.                                                                               |
+-----------------+--------------------------------------------------------------------------------------------------+
|`debug()`_       |Detailed debug information.                                                                       |
+-----------------+--------------------------------------------------------------------------------------------------+


方法
======
__construct()
-------------
构造函数

.. code-block:: php

  public function __construct (
      array $config = []
  )


:参数:
  +-------+-------------+
  |名称   |说明         |
  +=======+=============+
  |config |支持参数     |
  +-------+-------------+
  
  


__destruct()
------------
析构函数

.. code-block:: php

  public function __destruct ()



::

    关闭日志连接


log()
-----
可任意级别记录日志

.. code-block:: php

  public function log (
      string $level,
      string $message,
      array $context = []
  )


:参数:
  +--------+----------------+
  |名称    |说明            |
  +========+================+
  |level   |日志级别        |
  +--------+----------------+
  |message |日志内容        |
  +--------+----------------+
  |context |占位符内容      |
  +--------+----------------+
  
  


emergency()
-----------
System is unusable.

.. code-block:: php

  public function emergency (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


alert()
-------
Action must be taken immediately.

.. code-block:: php

  public function alert (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


::

    Example: Entire website down, database unavailable, etc. This should
    trigger the SMS alerts and wake you up.


critical()
----------
Critical conditions.

.. code-block:: php

  public function critical (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


::

    Example: Application component unavailable, unexpected exception.


error()
-------
Runtime errors that do not require immediate action but should typically
be logged and monitored.

.. code-block:: php

  public function error (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


warning()
---------
Exceptional occurrences that are not errors.

.. code-block:: php

  public function warning (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


::

    Example: Use of deprecated APIs, poor use of an API, undesirable things
    that are not necessarily wrong.


notice()
--------
Normal but significant events.

.. code-block:: php

  public function notice (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


info()
------
Interesting events.

.. code-block:: php

  public function info (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


::

    Example: User logs in, SQL logs.


debug()
-------
Detailed debug information.

.. code-block:: php

  public function debug (
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


