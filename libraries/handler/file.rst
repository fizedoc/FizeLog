============
文件形式
============


::

    文件形式日志类


+-------------+----------------------+
|属性         |值                    |
+=============+======================+
|命名空间     |fize\\log\\handler    |
+-------------+----------------------+
|类名         |File                  |
+-------------+----------------------+
|实现接口     |fize\\log\\LogHandler |
+-------------+----------------------+


:方法:


+-----------------+-------------+
|方法名           |说明         |
+=================+=============+
|`__construct()`_ |构造函数     |
+-----------------+-------------+
|`write()`_       |写入日志     |
+-----------------+-------------+


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
  +-------+-------+
  |名称   |说明   |
  +=======+=======+
  |config |参数   |
  +-------+-------+
  
  


write()
-------
写入日志

.. code-block:: php

  public function write (
      string $str,
      string $type = "INF",
      array $config = []
  ) : bool


:参数:
  +-------+-------------------------------+
  |名称   |说明                           |
  +=======+===============================+
  |str    |要写入的日志主体内容           |
  +-------+-------------------------------+
  |type   |日志类型，                     |
  +-------+-------------------------------+
  |config |传入的其他参数                 |
  +-------+-------------------------------+
  
  

