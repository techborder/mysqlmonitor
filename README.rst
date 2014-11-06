MySQL Monitor
=============

MySQL Monitor is a console-based (non-gui) tool for monitoring MySQL server.

MySQL Monitor is inspired by `innotop <http://code.google.com/p/innotop/>`_ and `mytop <http://jeremy.zawodny.com/mysql/mytop/>`_ .

Cloned from shoma's https://github.com/shoma/mysqlmonitor.

IMPROVEMENTS
------
- Changed sleep interval to be the same as given on command line argument. Added more info in help. 
- Added header to output. Lower processor resource consumed by increasing sleep time. 
- Changed default to append to a file instead of wiping it out.
- Added prompt for password when blank in arg list.
- Created separate methods to output different format, one with timestamp for troubleshooting.
- Cleaner output by removing columns in front of values of process list.


STATUS
------
**Tested working.**

REQUIREMENTS
------------

 - python2.7
 - MySQLdb. WARNING: If installing through apt-get, add ‘-s’ or ‘--simulate'. E.g. 'sudo apt-get --simulate install php5-mysqlnd' and make sure MySQL server is not removed. Else be very careful when installing MySQLdb through apt-get (aptitude), in one case, apt-get uninstalled mysql-server without asking for confirmation.

mysqlstaus.py
-------------

show status by *SHOW GLOBAL STATUS;* statement.

see `MySQL :: MySQL 5.1 Reference Manual :: 12.7.5.37 SHOW STATUS Syntax <http://dev.mysql.com/doc/refman/5.1/en/show-status.html>`_

::

    usage: mysqlstatus.py [-h [HOST]] [-p [PORT]] [-u [USER]] [-P [PASSWORD]]
                          [-i [INTERVAL]] [-o [OUTFILE]] [-n] [--help]
    
    optional arguments:
      -h [HOST], --host [HOST]
                        Connect to host.
      -p [PORT], --port [PORT]
                            Port number to use for connection.
      -u [USER], --user [USER]
                            User for login if not current user.
      -P [PASSWORD], --password [PASSWORD]
                            Password to use when connecting to server.
      -i [INTERVAL], --interval [INTERVAL]
                            Interval second of monitoring.
      -o [OUTFILE], --outfile [OUTFILE]
                            Output result file. avairable for non-interactive.
      -n, --nonint          Non-interactive.
      -m [{status,process}], --mode [{status,process}]
                                monitoring Mode
      --debug               Debug log enable.
      --help                show this help message and exit.

LICENSE
-------
MIT LICENSE
