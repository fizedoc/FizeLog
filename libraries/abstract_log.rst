===============
日志抽象类
===============


::

    提供了实际实现类需要的方法


+-------------+-------------------------------------------------+
|属性         |值                                               |
+=============+=================================================+
|命名空间     |fize\\log                                        |
+-------------+-------------------------------------------------+
|类名         |AbstractLog                                      |
+-------------+-------------------------------------------------+
|修饰符       |abstract                                         |
+-------------+-------------------------------------------------+
|父类         |Psr\\Log\\AbstractLogger                         |
+-------------+-------------------------------------------------+
|实现接口     |Psr\\Log\\LoggerInterface, fize\\log\\LogHandler |
+-------------+-------------------------------------------------+


:方法:


+-----------------+--------------------------------------------------------------------------------------------------+
|方法名           |说明                                                                                              |
+=================+==================================================================================================+
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
|`log()`_         |Logs with an arbitrary level.                                                                     |
+-----------------+--------------------------------------------------------------------------------------------------+
|`__construct()`_ |构造函数                                                                                          |
+-----------------+--------------------------------------------------------------------------------------------------+


方法
======
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
  
  


log()
-----
Logs with an arbitrary level.

.. code-block:: php

  abstract public function log (
      mixed $level,
      string $message,
      array $context = []
  ) : void


:参数:
  +--------+-------+
  |名称    |说明   |
  +========+=======+
  |level   |       |
  +--------+-------+
  |message |       |
  +--------+-------+
  |context |       |
  +--------+-------+
  
  


__construct()
-------------
构造函数

.. code-block:: php

  abstract public function __construct (
      array $config = []
  )


:参数:
  +-------+----------------------+
  |名称   |说明                  |
  +=======+======================+
  |config |初始化默认选项        |
  +-------+----------------------+
  
  


