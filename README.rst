Portcheck
=========

Utility to check if all commits in a git source branch are represented as ports
in the target branch

Usage
-----

::

  portcheck [-v] source-branch [target-branch]

Options
-------

- :code:`-v`: enables verbose mode
- :code:`source-branch`: branch containing commits that require port
- :code:`target-branch`: branch containing port commits

Ports
-----

Ports of commit :code:`commit-sha` are detected by having the following line in
the commit message:

::

  Port-of: commit-sha

The :code:`commit-sha` must be the complete SHA of the commit as returned by
:code:`git rev-parse ref`. The casing of the identifier is not significant.
