PCAN/PCAN FD系列驱动、API下载
==================================================

Windows驱动
------------
按照系统下载对应安装包，默认安装即可。驱动安装包包含PCAN-view软件，可进行报文收发和记录。

- `WIN10/11驱动下载`_
- `WIN8驱动下载`_
- `WIN7驱动下载`_
- `WIN XP驱动下载`_

.. _WIN10/11驱动下载: https://www.peak-system.com/quick/DrvSetup  
.. _WIN8驱动下载: https://www.peak-system.com/fileadmin/media/files/PEAK-System_Outdated-Driver-Setup_Win81.zip
.. _WIN7驱动下载: https://www.peak-system.com/fileadmin/media/files/PEAK-System_Outdated-Driver-Setup_Win7.zip
.. _WIN XP驱动下载: https://www.peak-system.com/fileadmin/media/files/PEAK-System_Outdated-Driver-Setup_WinXP.zip

二次开发包下载
------------------------
- 二次开发包 `PCAN-Basic(Windows)下载`_
- 二次开发包 `PCAN-Basic(Linux)下载`_


.. _PCAN-Basic(Windows)下载:  https://www.peak-system.com/fileadmin/media/files/pcan-basic.zip
.. _PCAN-Basic(Linux)下载:  https://www.peak-system.com/quick/BasicLinux

Linux驱动
------------
PCAN接口产品系列可与任何Linux操作系统完全兼容。

许多Linux发行版，或者说是使用的Linux内核，已经包含了PCAN的CAN接口的驱动程序。然后通过公共SocketCAN框架作为网络设备(又名netdev)访问CAN接口。



如果您正在使用缺少驱动程序的Linux环境(例如最小化的Linux环境，旧的内核)，或者您想使用我们的基于字符的驱动程序(chardev)，例如与PCAN- basic API连接，您需要我们的PCAN Linux驱动程序包，并自行编译驱动程序。

如何检查: 我的Linux环境是否已经包含PCAN 驱动?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

在命令行终端中输入

.. code-block:: bash

    grep PEAK_ /boot/config-`uname -r`

执行这条命令列出了所有的PEAK驱动程序(y =包含在内核中，m =单独的模块)。

如何检查: 我的PCAN CAN设备是否已经初始化?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

在命令行终端中输入
.. code-block:: bash

    lsmod | grep ^peak

如果连接并初始化了PCAN的CAN接口，则将至少有一行以peak_usb开头的输出