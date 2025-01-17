source_path
^^^^^^^^^^^

:Default value: `Disabled`
:Optional: Yes
:Values: * Absolute path on the local file system.
         * Relative path to the server installation folder.
:From version: 2.10.0
:To version: None
:Description:
    Path to the monitored source folder.


recursive
^^^^^^^^^

:Default value: `No`
:Optional: Yes
:From version: 2.10.0
:Values: * Yes
         * No
:Description:
    Determines whether the monitor should look for source files and folders
    only in the configured path, or recurse in all its descendant folders.


changes_poll_interval
^^^^^^^^^^^^^^^^^^^^^

:Default value: `10`
:Optional: Yes
:From version: 3.0.0
:Values: * Number of seconds.
:Description:
    This is the time interval that defines the delay used to observe
    the changes in the monitored path and compare snapshots, a record of any
    changes, in a monitored folder.


stable_interval
^^^^^^^^^^^^^^^

:Default value: `10`
:Optional: Yes
:From version: 2.10.0
:Values: * Number of seconds.
:Description:
    This is the interval after which a file is considered stable if no changes
    are made to it.


source_filter
^^^^^^^^^^^^^

:Default value: `Disabled`
:Optional: Yes
:From version: 2.10.0
:Values: * `Globbing expression containing wildcard characters`.
         * `Regular expression`
         * `Disabled`
         * Empty
:Description:
    `Globbing expression
    <http://en.wikipedia.org/wiki/Glob_%28programming%29>`_ or
    `regular expression <http://en.wikipedia.org/wiki/Regular_expression>`_
    used to select source files to be transferred.
    For more details see the :doc:`matching expression
    documentation</configuration/matching-expression>`

    Only files matching the expression will be transferred.

    A globing expression can contain multiple filemask filtering rules,
    separated by the pipe character `|`.

    Only file names are filtered, all folder names will be transferred.

    Leave it empty or set it to `Disabled` to transfer all files.
